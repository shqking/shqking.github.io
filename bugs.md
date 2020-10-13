---
layout: post
title: BUGS
---

- FFmpeg
  - DoS issues, which might cause huge CPU and/or memory consumption ([CVE-2017-14054](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14054), [CVE-2017-14055](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14055), [CVE-2017-14056](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14056), [CVE-2017-14057](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14057), [CVE-2017-14059](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14059), [CVE-2017-14170](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14170), [CVE-2017-14171](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14171), [CVE-2017-14222](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14222), [CVE-2017-14223](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14223))
  - infinite loop ([CVE-2017-14058](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14058))
  - integer signedness error, which might bypass a security check ([CVE-2017-14169](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14169))
- ImageMagick
  - DoS issues ([CVE-2017-14172](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14172), [CVE-2017-14174](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14174), [CVE-2017-14175](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14175))
  - infinite loop([CVE-2017-14173](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14173))
  - invalid loop condition in `coders/mat.c`, which might block legatimate inputs [[bug report]](https://github.com/ImageMagick/ImageMagick/issues/745) [[fix]](https://github.com/ImageMagick/ImageMagick/commit/631d3ad01a6fe80ddaed5318c549c2bdb092f9ee)
- GraphicsMagick
  - null pointer dereference vulnerability in `coders/png.c` [[bug report]](https://sourceforge.net/p/graphicsmagick/bugs/426/) [[fix]](https://sourceforge.net/p/graphicsmagick/code/ci/22d4cdbbed38655cac687524162f8d2694cb6d28/) 
  - buffer overflow vulnerability in `coders/pict.c:ReadPICTImage()` [[bug report]](https://sourceforge.net/p/graphicsmagick/bugs/427/) [[fix]](https://sourceforge.net/p/graphicsmagick/code/ci/b1afa3e8f0ab57aa7395f37a8025c7389c2021b7/)
  - DoS issues in `xbm.c: ReadXBMImage()` and `jnx.c:ReadJNXImage()` ([CVE-2017-13775](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-13775), [CVE-2017-13776](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-13776), [CVE-2017-13777](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-13777))
- ImageWorsener
  - uninitialized variable in `src/imagew-gif.c`, which might cause unspecified program behavior [[bug report]](https://github.com/jsummers/imageworsener/issues/28) [[fix]](https://github.com/jsummers/imageworsener/commit/edf0db37b208d0db0dc135fe0acf21f8216a1fd3)
- Linux kernel
  - integer overflow in `drivers/scsi/qla2xxx/qla_attr.c` ([CVE-2017-14051](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14051))
- Vim
  - integer overflow in `spellfile.c` ([CVE-2017-5953](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5953))
  - two integer overflows in `undo.c` ([CVE-2017-6349](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-6349), [CVE-2017-6350](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-6350))
- Xemacs
  - integer overflow vulnerability in `src/lread.c` [[link]](https://bitbucket.org/xemacs/xemacs/commits/0ae4d70)
- Apache httpd
  - stack address returned in `support/htpasswd.c`, one kind of information leak vulenrability, which might leak stack address out of current function frame [[bug report]](https://bz.apache.org/bugzilla/show_bug.cgi?id=60634) [[fix]](https://svn.apache.org/viewvc?view=revision&revision=1781509)
- libgd
  - memory leak vulnerability in `src/gdft.c:gdImageStringFTEx()`, i.e., the allocated memory is not freed on certain path [[fix]](https://github.com/libgd/libgd/commit/5176856eae3b50fa82a6dc4518e908be0699837c)
- Wireshark
  - resource leak vulnerability in `plugins/profinet/packet-dcerpc-pn-io.c:dissect_ExpectedSubmoduleBlockReq_block()`, i.e., the opened file is not closed properly [[bug report]](https://bugs.wireshark.org/bugzilla/show_bug.cgi?id=13826) [[fix]](https://code.wireshark.org/review/gitweb?p=wireshark.git;a=blobdiff;f=plugins/profinet/packet-dcerpc-pn-io.c;h=b00aa3f69a3950397ce7046f1be89ed50f22cefc;hp=fd1bb51ad9f15da69aca692cc720e9047d055d22;hb=84ee66b9bc97bfa294f11b4083f8f09b115c17e0;hpb=a24f366ceb8eccf2e3a0501a394653c9eb6bed83)
- Rsync
  - integer overflow in `xattrs.c:692`, which might lead to buffer overrun [[bug report]](https://bugzilla.samba.org/show_bug.cgi?id=12568) [[fix]](https://git.samba.org/?p=rsync.git;a=commit;h=3fb1634f21fdad145eb30d9387e7f8d48f1f7692)
- Net-snmp
  - four memory leak vulnerabilities in `nsLogging.c,snmpNotifyFilterProfileTable.c,tcpTable.c,nsCache.c`. That is, the allocated memory is not freed on certain exceptional execution path [[bug report]](https://sourceforge.net/p/net-snmp/bugs/2788/) [[fix]](https://sourceforge.net/p/net-snmp/code/ci/bba1451f8ae64e3f58986408041a28f8e34e6f35/)
- Memcached
  - use of uninitialized array in `items.c: lru_maintainer_thread()` [[bug report]](https://github.com/memcached/memcached/issues/310) [[fix]](https://github.com/memcached/memcached/commit/a906f77ebda87c339da6160fb01bf5694555d24d)
- Bento4
  - two resource leak vulnerabilities in `Source/C++/Apps/Mp4Mux/Mp4Mux.cpp` [[bug report]](https://github.com/axiomatic-systems/Bento4/issues/222#issuecomment-342816421) [[fix]](https://github.com/axiomatic-systems/Bento4/commit/92ed8ace9c7c67b31563beaf25800e1a8622eb7d)
- Qemu
  - stack address returned in `target-s390x/translate.c`, one kind of information leak vulenrability, which might leak stack address out of current function frame [[bug report]](https://bugs.launchpad.net/qemu/+bug/1661815)[[fix]](https://lists.gnu.org/archive/html/qemu-devel/2020-01/msg05204.html)