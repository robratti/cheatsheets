# Curl Cheatsheet

| Command Description                                | Command Example |
|----------------------------------------------------|-----------------|
| **Basic Usage**                                    | `curl [options...] <url>` |
| **HTTP GET Request**                               | `curl http://example.com` |
| **HTTP POST Request**                              | `curl -X POST -d "param1=value1&param2=value2" http://example.com` |
| **HTTP POST Request with JSON**                    | `curl -X POST -H "Content-Type: application/json" -d '{"key1":"value1", "key2":"value2"}' http://example.com` |
| **Adding Headers**                                 | `curl -H "Authorization: Bearer token" http://example.com` |
| **Follow Redirects**                               | `curl -L http://example.com` |
| **Save Response to a File**                        | `curl -o output.txt http://example.com` |
| **FTP Download**                                   | `curl ftp://ftp.example.com/file.txt -o file.txt` |
| **FTP Upload**                                     | `curl -T file.txt ftp://ftp.example.com/ --user username:password` |
| **SFTP Upload**                                    | `curl -T file.txt sftp://example.com/ --user username:password` |
| **SMTP Send Email**                                | `curl smtp://mail.example.com --mail-from "from@example.com" --mail-rcpt "to@example.com" --upload-file email.txt` |
| **Verbose Output**                                 | `curl -v http://example.com` |
| **Silent Mode**                                    | `curl -s http://example.com` |
| **Limit Download Speed**                           | `curl --limit-rate 100K http://example.com` |
| **Specify User Agent**                             | `curl -A "Mozilla/5.0" http://example.com` |
| **Use Proxy**                                      | `curl -x http://proxy.example.com:8080 http://example.com` |
| **Use SOCKS Proxy**                                | `curl --socks5 hostname:port http://example.com` |
| **HTTP Basic Authentication**                      | `curl --user username:password http://example.com` |
| **Upload File**                                    | `curl -F "file=@/path/to/file" http://example.com/upload` |
| **Download Only Headers**                          | `curl -I http://example.com` |
| **Set Request Timeout**                            | `curl --max-time 10 http://example.com` |
| **Follow Redirects and Get Final URL**             | `curl -Ls -o /dev/null -w %{url_effective} http://example.com` |
| **Send Cookies**                                   | `curl -b "name1=value1; name2=value2" http://example.com` |
| **Save Cookies**                                   | `curl -c cookies.txt http://example.com` |
| **Telnet**                                         | `curl -vvv telnet://example.com:23` |
| **Resolve Hostname to Specific IP**                | `curl --resolve example.com:80:127.0.0.1 http://example.com` |
| **Download via SCP**                               | `curl -u username scp://example.com//path/to/file` |
| **Download via SFTP**                              | `curl -u username sftp://example.com/path/to/file` |
| **HTTP DELETE Request**                            | `curl -X DELETE http://example.com/resource` |
| **HTTP PUT Request**                               | `curl -X PUT -d "param1=value1" http://example.com/resource` |
| **Download and Resume**                            | `curl -C - -o file.zip http://example.com/file.zip` |
| **Disable SSL Certificate Verification**           | `curl -k https://example.com` |
| **Pass Client Certificate**                        | `curl --cert /path/to/cert.pem --key /path/to/key.pem https://example.com` |
