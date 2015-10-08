## Troubleshooting Cntlm

If you have trouble with Cntlm and don't know if you are actually getting to the proxy. The easiest way to diagnose the problem is to run Cntlm in foreground

1. Stop the `Cntlm Authentication Proxy` service

2. Open a command windows.

3. Move to the directory where the cntlm.exe is located. Usually C:\Program Files (x86)\Cntlm\cntlm.exe. 	

	Run:
```
> cntlm -f
```

On the command window you will see somethin like this:

```
C:\Users\lberrocal>cd "C:\Program Files (x86)\Cntlm"

C:\Program Files (x86)\Cntlm>cntlm.exe -f
      2 [main] cntlm 9672 find_fast_cwd: WARNING: Couldn't compute FAST_CWD pointer.  Please report this problem to
the public mailing list cygwin@cygwin.com
cygwin warning:
  MS-DOS style path detected: C:\Program Files (x86)\Cntlm\cntlm.ini
  Preferred POSIX equivalent is: /Cntlm/cntlm.ini
  CYGWIN environment variable option "nodosfilewarning" turns off this warning.
  Consult the user's guide for more details about POSIX paths:
    http://cygwin.com/cygwin-ug-net/using.html#using-pathnames
cntlm: PID 9672: Cntlm ready, staying in the foreground
cntlm: PID 9672: Using proxy procuratio.canal.acp:8080
cntlm: PID 9672: 127.0.0.1 CONNECT live.github.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT live.github.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT ssl.gstatic.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT www.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT www.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT outlook.office365.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT outlook.office365.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT clients5.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT plus.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT outlook.office365.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT play.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT play.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT accounts.google.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT googleads.g.doubleclick.net:443
cntlm: PID 9672: 127.0.0.1 CONNECT outlook.office365.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT outlook.office365.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT www.gitbook.com:443
cntlm: PID 9672: 127.0.0.1 CONNECT platform.twitter.com:443cntlm: PID 9672: 127.0.0.1 CONNECT js.stripe.com:443cntlm: PI
cntlm: PID 9672: 127.0.0.1 CONNECT sm3lir.cloudimage.io:443 127.0.0.1 CONNECT platform.twitter.com:443cntlm: PID 9672: 1
27.0.0.1 CONNECT sm3lir.cloudimage.io:443
```
This readout shows your computer is accesing the Internet through the proxy.

If you don't see any activity check your cntlm.ini you probably have something wrong in your configuration. The most common problem is a wrong password.