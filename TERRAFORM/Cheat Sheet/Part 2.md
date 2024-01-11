# TERAFORM CHAETSHEET

## PLAN, DEPLOY AND CLEANUP INFRASTRUCTURE
- terraform apply--auto-approve: apply changes without being prompted to enter 'yes'
- terraform destroy--auto-approve: destroy/cleanup deployment without being prompted for 'yes'
- transform plan-out plan.out: output the deployment plan to plan out
- terraform apply plan.out: use the plan out plan file to deply infrastructure
- terraform plan-destroy: outputs a destroy plan
- terraform apply-target=aws_instance.my_ec2: only apply/deploy changes to the targeted resource
- terraform apply-var my_region_variables=us-east-1: pass a variable via command-line while applying a configuration.
- terraform apply-lock=true: lock the state file so it can't be modified by any other Terraform apply or modification action 
 (possible only where backend allows locking)
- terraform apply refresh=false: do not reconcile state file with real-world resources(helpful with large complex deployments for saving deployment time)
- terraform apply --parrellelism=5: number of simultaneous resource operations
- terraform refresh: reconcile the state in terraform state file with real world resources
- terraform providers: get information about providers used in current configuration

## TERRAFORM WORKSPACES
- terraform workspace new mynewworkspace: create a new workspace
- terraform workspace select default: change to the selected workspace
- terraform workspace list: list out all workspaces

## TRANSFORM STATE MANIPULATION
- tertaform state show aws_instance.my_ec2: show details stored in terraform state for the resource
- terraform state pull>terraform.tfstate: download and output terraform state to a file
- terraform state mv aws_iam_role.my_ssm_rolemodule.custom_module: move a resource tracked via state to different module
- terraform state replace-provider hashicorp/aws registry.custom.com/aws: replace existing provider with another
- transform state list: list all the resources tracked in the current state file
- terraform state rm aws_instance.myinstance: unmanage a resource, delete it from Terraform state file.

## TERRAFORM IMPORT AND OUTPUT
- terraform import aws_instance.new_ec2_instance i-abcd1234: import EC2 instance with id i-abcd1234 into the terraform 
  resource named "new_ec2_instance" of type "aws_instance"
- terraform import 'aws_instance.new_ec2_instance[0]'i-abcd1234: same as above, imports a real-world resource into an instance of terraform resource
- terraform ouput: list all ouputs as stated in code
- terraform output instance_public_ip: list a specific declared output
- terraform output-json: list all ouputs in JSON format

## TERRAFORM CLI TRICKS
- terraform -install-autocomplete: setup tab auto-completion, requires logging back in

## FORMAT AND VALIDATE TERRAFROM CODE
- terraform fmt: format code per HCL canonical standard
- terraform validate: validate code for syntax
- terraform validate-backend=false: validate code skip backend validation

##  INITIALIZE YOUR TERRAFORM WORKING DIRECTORY
- terrafrom init: initailize directory, pull down providers
- terraform init -get-plugins=false: initialize directory, do not download plugins
- terraform init -verify-plugins=false: initialize directory, do not verify plugins for Hashicorp signature

## TERRAFORM MISCELLANEOUS COMMANDS
- terraform version: display terraform binary version, also warns if version is old.
- terraform get -update=true: download and update modules in the 'root' module.

## TERRAFORM CONSOLE (TEST OUT TERRAFORM INTERPOLATIONS)
- echo 'join[",",["foo","bar"]]' | terraform console: echo an expression into terraform console and see its expected result as output 
- echo '1 + 5'| terraform console: terraform console also has an interactive CLI just enter 'transform console'
- echo "aws_instance.my_ec2.public_ip" | terraform console: display the public IP against the "my_ec2" terraform as seen in the Terrafrom state file

## TERRAFROM GRAPH (DEPENDENCY GRAPHING)
- terraform graph|dot-Tpng>graph.png: produce a PNG diagram showing relationship and dependencies between terraform resources in your 
  configuration/code
  
## TERRAFORM TAINT/UNTAINT
- terraform taint aws_instance.my_ec2: taint resource to be recreated on next apply
- terraform untaint aws_instance.myec2: remove taint from a resource
- terraform force-unlock LOCK-ID: force unlock a locked state file, LOCK_ID provided when locking the state file beforehand

## TRANSFORM CLOUD 
- transform login: obtain and save API token for terraform cloud
- terraform logout: log out of terraform cloud, defaults to hostname app.terraform.io
