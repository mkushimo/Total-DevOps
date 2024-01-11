This is a Linux command line reference for common operations. 
Examples marked with * are valid/safe to paste without modification into a terminal so, you may want to keep
a terminal window window open while reading this so you can cut & paste. See also more linux commands.

| COMMAND | DESCRIPTION |
| :--- | :--- |
| apropos whatis | show commands pertinent to string. see alsoo threadsafe |
| man -t man l ps2pdf -> man.pdf | make a pdf of a manual page |
| which command | show full path name of command |
| time command | see how long a command takes |
| time cat | start stopwatch. ctrl + d to stop. see also sw. |

## DIR NAVIGATION 
| COMMAND | DESCRIPTION |
| :--- | :--- |
| cd- | go to previous directory |
| cd | go to $HOME directory |
| (cd dir && command) | go to dir, execute command and return to current dir |
| pushd. | put current dir on stack so you can popd vback to it |

## FILE SEARCHING
| COMMAND | DESCRIPTION |
| :--- | :--- |
| alias l='ls-l--color=auto' | quick dir listing |
| ls-lrt | list files by date. see also newest and find_mm_yyy |
| ls/usr/bin l pr-T9-W$COLUMNS | print in 9 columns to width of terminal |
| find -name '*.[ch]' l xargs grep -E 'expr' | search 'expr' in this dir and below. see also findrepo |
| find -type f -print0 l xargs -r0 grep -F 'example' | search all regular files for 'example' in this dir and below |
| find -maxdepth 1 -type f l xargs drep -F 'exammple' | search all regular files for 'example' in this dir |
| find -maxdepth 1 -type d l while read dir; do echo $dir; echo  cmd2; done | process each item with multiple commands (in while loop) |
| find -type f! -perm -444 | find files not readable by all (useful for website) |
| find -type d! -perm -111 | find dirs not accessible by all (useful for website) |
| locate -r 'file[^/]*\txt' | search cached index forn names. This re is like glob *file*.txt |
| look reference | quickly search (sorted) dictionary for prefix |
| grep --color reference/usr/share/dict/words | highlight occurences of regular  expression in dictionary |

## ARCHIVES AND COMPRESSION
| COMMAND | DESCRIPTION |
| :--- | :--- |
| gpg -c file | encrypt file |
| gpg file.gpg | decrypt file |
| tar -c dir/ l bzip2 > dir.tar.bz2 | make compressed archive of dir/ |
| bzip2 -dc dir.tab.bz2 l tar -x | extract archive (use gzip instead of bzip2 for tar.gz files) |
| tar -c dir/ l gzip l gpg -c l ssh user@remote 'dd of=dir.tar.gz.gpg' | make encrypted archive of dir/ on remote machine |
| find dir/ -name '*.txt' l tar -c--files-from=- l bzip2 > dir_txt.tar.bz2 | make archive of subset of dir/ and below |
| find dir/ -name '*.txt' l xargs cp -a --target-directory=dir_txt/--parents | make copy of subset of dir/ and below |
| (tar-c/dir/to/copy) l (cd/where/to/&&tar-x-p) | copy (with permissions) copy/dir to/where/to/dir |
| (cd/dir/to/copy&&tar-c.) l (cd/where/to/&&tar-x-p) | copy (with permissions) contents of copy/dir to where/to/ |
| (tar-c/dir/to/copy) l ssh -C user@remote 'cd/where/to/&&tar-x-p' | copy (with permissions) copy/dir to remote:/where/to/dir |
| dd bs=1M if=/dev/sda l gzip  l ssh user@remote 'dd of =sda.gz' | backup harddisk to remote machine |

## rsync (Network efficient file copier:use the --dry-run option forb testing)
| COMMAND | DESCRIPTION |
| :--- | :--- |
| rsync -P rsync://rsync.server.com/path/to/file file | only get diffs. do multiple times for troublesome downloads |
| rsync --bwlimit=1000 fromfile tofile | locally copy with rate limit. It's like nice for I/o |
| rsync -az -e ssh --delete~/pubic_html/remote.com'~/public_html' | mirror website (using compression and encryption ) |
| rsync -auz -e ssh remote:/dir/.&&rsync-auz-e ssh.remote:/dir/ | synchronize current directory with remote one |

## ssh (secure shell)
| COMMAND | DESCRIPTION |
| :--- | :--- |
| ssh $USER@HOST command | run command on $HOST as $USER (default command=shell) |
| ssh -f -Y$USER@$HOSTNAMExeyes | run GUI command on $HOSTNAME as $USER |
| scp -p-r$USER@HOST:file dir/ | copy with permissions to $USER's home directory on $HOST |
| ssh -g -L 8080:localhost:80 root@$HOST | forward connections to $HOSTNAME:8080 out to $HOST:80 |
| ssh -R 1434:imap:143 root@$HOST | forward connections from $HOST:1434 in to imap:143 |
| ssh-copy-id$USER@$HOST | install $USER's public key on $HOST for password-less login |

## wget (multi-purpose download tool)
| COMMAND | DESCRIPTION |
| :--- | :--- |
| (cd dir/ && wget -nd
