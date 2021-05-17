# send_vuln_pkgs_after_cvescan

Tool for parse report from cvescan and send to syslog server or file

1) download cvescan OR https://github.com/qwerty1q2w/make_cvescan_bin
2) Run cvescan - /snap/bin/cvescan --priority all --json > path_to_cvescan_report
3) Run this tool - ./cvescan_handler -o file -rp path_to_cvescan_report ###Output in /var/log/vulners.log
4) OR send to syslog - ./cvescan_handler -o syslog -rp path_to_cvescan_report -s syslog_server_ip -p port

DEBIAN and etc folder for create deb package with cvescan




output example

'''
{"cve_id": "CVE-2021-25216", "fixed_ver": "1:9.11.3+dfsg-1ubuntu1.15", "host_name": "kub2", "installed_ver": "1:9.11.3+dfsg-1ubuntu1.14", "os": "18.04", "pkg_name": "libisccc160", "priority": "medium", "timestamp": "2021-05-17T07:07:31.060402"}
'''
