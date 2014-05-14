# lsof

In this cheat sheet, I will list some commonly used lsof commands.


## 1. Get information about a (list of) file(s)

> lsof /path/to/file [ /path/to/other/file ... ]


## 2. List files opened by a specific user(s)(id('s))

> lsof -u [^]<username or uid> [ ,<other username or uid>,... ]

Generally '^' inverts the selection.


## 3. Show open files in a directory recursively

> lsof +D </path/to/directory>


## 4. Open files by program name

> lsof -c <program name>


## 5. Same thing by process id

> lsof -p <pid>


## Sources

  - http://www.catonmat.net/blog/unix-utilities-lsof/
