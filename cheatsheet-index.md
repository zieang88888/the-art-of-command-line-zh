# 命令行艺术 · 全量章节中文索引

> 源项目：[jlevy/the-art-of-command-line](https://github.com/jlevy/the-art-of-command-line)（master 分支 README）
> 本索引仅做中文导读，条目名称均来自源 README 实测；统计日期 2026-10-06。共 **9 个内容章节、211 条技巧/命令**。

---

## 1. Meta · 元说明（6 条说明性内容，不计入技巧总数）

- 适用范围：面向初学者与有经验用户，追求广度 / 具体性 / 简洁性
- 面向 Linux，另设 macOS only / Windows only 专章
- 聚焦交互式 Bash，兼顾 Bash 脚本
- 同时收录标准 Unix 命令与需额外安装的重要工具
- 单页原则：细节自行 Google，用 `apt`/`yum`/`dnf`/`pacman`/`pip`/`brew` 安装
- 用 [Explainshell](http://explainshell.com/) 拆解命令、参数与管道

## 2. Basics · 基础（12 条）

1. 学基础 Bash：`man bash` 通读一遍
2. 精通至少一款文本编辑器：`nano` / `vi`(Vim) / Emacs
3. 查文档：`man`、`man man`、`apropos`、`help`、`type`、`curl cheat.sh/<cmd>`
4. 输入输出重定向与管道：`>`、`>>`、`<`、`|`、stdout/stderr
5. 通配符展开 `* ? [...]` 与引号 `"..."` / `'...'`
6. Bash 任务管理：`&`、Ctrl-Z、Ctrl-C、`jobs`、`fg`、`bg`、`kill`
7. `ssh` 与免密登录：`ssh-agent`、`ssh-add`
8. 基础文件管理：`ls -l`、`less`、`head`、`tail -f`、`ln -s`、`chown`、`chmod`、`du -hs *`、`df`、`mount`、`fdisk`、`lsblk`、inode
9. 基础网络管理：`ip`/`ifconfig`、`dig`、`traceroute`、`route`
10. 版本控制系统：`git`
11. 正则表达式与 `grep`/`egrep`：`-i -o -v -A -B -C`
12. 包管理：`apt-get`/`yum`/`dnf`/`pacman` 与 `pip`

## 3. Everyday use · 日常使用（44 条）

1. Tab 补全；`Ctrl-R` 搜索历史
2. 行内快捷键：`Ctrl-W` `Ctrl-U` `Alt-B` `Alt-F` `Ctrl-A` `Ctrl-E` `Ctrl-K` `Ctrl-L` `Alt-.` `Alt-*`
3. `set -o vi` / `set -o emacs` 切换键位风格
4. `Ctrl-X Ctrl-E`（或 `Esc-V`）在编辑器中编辑长命令
5. `history`、`!n`、`!$`、`!!`
6. `cd`、`~`、`$HOME`
7. `cd -` 回到上一目录
8. `Alt-#` 把半截命令注释掉留待后用
9. `xargs` / `parallel`（`-L` `-P` `-I{}`）
10. `pstree -p` 进程树
11. `pgrep` / `pkill`（`-f`）
12. 进程信号：`kill -STOP`、`man 7 signal`
13. `nohup` / `disown` 后台常驻
14. 查看监听端口：`netstat -lntp` / `ss -plat` / `lsof -iTCP -sTCP:LISTEN`
15. `lsof` / `fuser` 查打开的套接字与文件
16. `uptime` / `w`
17. `alias` 别名
18. 把别名/配置写入 `~/.bashrc`
19. 登录环境变量写 `~/.bash_profile`
20. 用 Git 同步多机配置文件
21. 空格与文件名安全：引号 `"$FOO"`、`-0`/`-print0`、`IFS=$'\n'`
22. 脚本严格模式：`set -x`、`set -euo pipefail`、`trap ... ERR`
23. 子shell `(cd /other && cmd)`
24. 变量展开：`${name:?}`、`${name:-default}`、`$((...))`、`{1..10}`、`${var%suffix}`
25. 大括号展开 `mv foo.{txt,pdf} dir`
26. 展开顺序：brace → tilde/param/arith/cmdsub → word splitting → filename
27. 进程替换 `<(cmd)`
28. 脚本整体包在 `{ }` 中防半截执行
29. here document `cat <<EOF`
30. 合并 stdout/stderr：`cmd >log 2>&1` / `&>log`，并加 `</dev/null`
31. `man ascii` / `man unicode` / `man utf-8`
32. 终端复用：`screen` / `tmux` / `byobu` / `dtach`
33. SSH 端口隧道：`-L` `-D` `-R`
34. `~/.ssh/config` 保活/压缩/多路复用优化
35. 谨慎项：`StrictHostKeyChecking=no`、`ForwardAgent=yes`
36. `mosh`（UDP，抗断线）
37. `stat -c '%A %a %n'` 查八进制权限
38. 交互式选择：`percol` / `fzf`
39. `fpp`（PathPicker）基于输出选文件
40. 临时静态服务器：`python -m http.server 7777`
41. `sudo`（`-u`、`-i`）
42. `su username` / `su - username`
43. 128K 参数长度上限（Argument list too long）→ 用 `find`/`xargs`
44. `python` 当计算器

## 4. Processing files and data · 文件与数据处理（35 条）

1. 按名找文件：`find . -iname` / `locate`（`updatedb`）
2. 更快的搜索：`ack` / `ag`(The Silver Searcher) / `rg`(ripgrep)
3. HTML 转文本：`lynx -dump -stdin`
4. 文档转换：`pandoc`
5. XML：`xmlstarlet`
6. JSON：`jq`（交互 `jid` / `jiq`）
7. YAML：`shyaml`
8. CSV/Excel：`csvkit`（`in2csv` `csvcut` `csvjoin` `csvgrep`）
9. S3/AWS：`s3cmd` / `s4cmd` / `aws` / `saws`
10. `sort` / `uniq`（`-u` `-d`）/ `comm`
11. `cut` / `paste` / `join`
12. `wc`（`-l -m -w -c`）
13. `tee`
14. 统计计算：`datamash`
15. locale 影响排序与性能：`LC_ALL=C`
16. 命令前加环境变量：`TZ=Pacific/Fiji date`
17. 基础 `awk` / `sed`
18. 批量替换：`perl -pi.bak -e 's/old/new/g'`
19. 批量重命名/替换：`repren` / `rename`
20. `rsync`（同步、断点续传、批量删文件）
21. 进度监控：`pv` / `pycp` / `pmonitor` / `progress` / `dd status=progress`
22. `shuf` 随机抽样
23. `sort` 选项：`-n` `-h` `-t` `-k1,1` `-s`
24. 输入字面 Tab：`Ctrl-V Tab` 或 `$'\t'`
25. 补丁：`diff` / `patch` / `diffstat` / `sdiff` / `vimdiff`
26. 二进制查看/编辑：`hd` / `hexdump` / `xxd` / `bvi` / `hexedit`
27. `strings` 从二进制提取文本
28. 二进制差异：`xdelta3`
29. 编码转换：`iconv` / `uconv`
30. 切分文件：`split` / `csplit`
31. 日期时间：`date -u +%Y-%m-%dT%H:%M:%SZ`、`dateutils`
32. 压缩文件操作：`zless` / `zmore` / `zcat` / `zgrep`
33. 文件属性：`chattr +i` 防误删
34. ACL 备份恢复：`getfacl` / `setfacl`
35. 快速建空文件：`truncate` / `fallocate` / `xfs_mkfile` / `mkfile`

## 5. System debugging · 系统调试（20 条）

1. Web 调试：`curl` / `curl -I` / `wget` / `httpie`
2. CPU/磁盘：`top` / `htop` / `iostat` / `iotop`
3. 网络连接：`netstat` / `ss`
4. 全局概览：`dstat` / `glances`
5. 内存：`free` / `vmstat`（理解 cached）
6. Java 调试：`kill -3`、`jps`/`jstat`/`jstack`/`jmap`、SJK
7. `mtr` 更好的 traceroute
8. 磁盘占用：`ncdu`
9. 带宽占用：`iftop` / `nethogs`
10. 压测：`ab` / `siege`
11. 抓包：`wireshark` / `tshark` / `ngrep`
12. `strace` / `ltrace`（`-c` `-p` `-f`）
13. `ldd` 查共享库（勿对不可信文件运行）
14. `gdb` attach 进程看栈
15. `/proc`（`cpuinfo` `meminfo` `cmdline` `cwd` `exe` `fd` `smaps`）
16. `sar` 历史性能数据
17. 深度分析：`stap`(SystemTap) / `perf` / `sysdig`
18. 系统信息：`uname -a` / `lsb_release -a`
19. `dmesg` 查硬件/驱动问题
20. 删文件空间未释放：`lsof | grep deleted`

## 6. One-liners · 一行流（8 条）

1. 集合运算：`sort a b | uniq`（并集）/ `uniq -d`（交集）/ `uniq -u`（差集）
2. 美化 diff 两个 JSON：`diff <(jq --sort-keys . a) <(jq --sort-keys . b) | colordiff | less -R`
3. 快速浏览目录：`grep . *` / `head -100 *`
4. 列求和：`awk '{x+=$3} END{print x}' file`
5. 递归文件清单：`find . -type f -ls`
6. 日志统计：`egrep -o 'acct_id=[0-9]+' log | cut -d= -f2 | sort | uniq -c | sort -rn`
7. 持续监控：`watch -d -n 2 'ls -rtlh | tail'`
8. 随机抽一条本指南：`taocl()` 函数（curl + pandoc + xmlstarlet）

## 7. Obscure but useful · 冷门但有用（72 条）

`expr` · `m4` · `yes` · `cal` · `env` · `printenv` · `look` · `cut/paste/join` · `fmt` · `pr` · `fold` · `column` · `expand/unexpand` · `nl` · `seq` · `bc` · `factor` · `gpg` · `toe` · `nc` · `socat` · `slurm` · `dd` · `file` · `tree` · `stat` · `time` · `timeout` · `lockfile` · `logrotate` · `watch` · `when-changed` · `tac` · `comm` · `strings` · `tr` · `iconv/uconv` · `split/csplit` · `sponge` · `units` · `apg` · `xz` · `ldd` · `nm` · `ab/wrk` · `strace` · `mtr` · `cssh` · `rsync` · `wireshark/tshark` · `ngrep` · `host/dig` · `lsof` · `dstat` · `glances` · `iostat` · `mpstat` · `vmstat` · `htop` · `last` · `w` · `id` · `sar` · `iftop/nethogs` · `ss` · `dmesg` · `sysctl` · `hdparm` · `lsblk` · `lshw/lscpu/lspci/lsusb/dmidecode` · `lsmod/modinfo` · `fortune/ddate/sl`

## 8. macOS only · 仅 macOS（7 条）

1. 包管理：`brew`(Homebrew) / `port`(MacPorts)
2. 剪贴板：`pbcopy` / `pbpaste`
3. Terminal 把 Option 当作 Meta 键
4. 用桌面应用打开文件：`open` / `open -a`
5. Spotlight：`mdfind` / `mdls`
6. BSD 版命令与 GNU 版差异（`ps` `ls` `tail` `awk` `sed`），可装 `gawk`/`gsed`
7. 系统版本：`sw_vers`

## 9. Windows only · 仅 Windows（13 条）

**获取 Unix 工具（4）**：Cygwin · WSL · MinGW/MSYS · Cash
**Windows 原生命令行工具（3）**：`wmic` · `ping`/`ipconfig`/`tracert`/`netstat` · `Rundll32`
**Cygwin 技巧（6）**：包管理器装软件 · `mintty` 终端 · `/dev/clipboard` 剪贴板 · `cygstart` 打开文件 · `regtool` 注册表 · `cygpath` 路径转换

---

> 完整原文（含示例与详细说明）请回到源仓库 [jlevy/the-art-of-command-line](https://github.com/jlevy/the-art-of-command-line) 阅读。
