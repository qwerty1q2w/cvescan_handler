# send_vuln_pkgs_after_cvescan

Tool for parse report from cvescan and send to syslog server or file

1) download cvescan OR https://github.com/qwerty1q2w/make_cvescan_bin
2) Run cvescan - /snap/bin/cvescan --priority all --json > path_to_cvescan_report
3) Run this tool - ./cvescan_handler -o file -rp path_to_cvescan_report ###Output in /var/log/vulners.log
4) OR send to syslog - ./cvescan_handler -o syslog -rp path_to_cvescan_report -s syslog_server_ip -p port
