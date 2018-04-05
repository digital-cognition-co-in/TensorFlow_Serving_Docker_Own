### Logging almost everything - while Installing Docker image for TF Serving CPU on Xenial 16 
#
#

``` python

dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
[sudo] password for dhankar: 
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS                      PORTS               NAMES
c2124e6f3fc5        tensorflow/tensorflow             "/run_jupyter.sh --a…"   42 minutes ago      Exited (0) 31 minutes ago                       serene_chandrasekhar
2c406ec20315        ddrohit/new_image_ubuntu_qgis_3   "bash"                   13 days ago         Exited (127) 13 days ago                        cranky_heisenberg
51222fc2ea78        ddrohit/new_image_ubuntu_qgis_2   "bash"                   13 days ago         Exited (0) 13 days ago                          elastic_colden
1ac88cc06e5f        ddrohit/new_image_ubuntu_qgis_2   "bash"                   13 days ago         Exited (139) 13 days ago                        goofy_hopper
3501e1023cf0        ddrohit/new_image_ubuntu_qgis_2   "bash"                   13 days ago         Exited (2) 13 days ago                          naughty_murdock
6d3c3634ca4f        ddrohit/new_image_ubuntu_qgis_1   "bash"                   2 weeks ago         Exited (1) 2 weeks ago                          eloquent_engelbart1
5c2ed1274cc4        ddrohit/new_image_ubuntu_qgis_1   "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis     "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis     "bash"                   2 weeks ago         Exited (1) 2 weeks ago                          agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1        "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu          "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        sleepy_northcutt
82d279189cbf        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          kind_hugle
8c124734e956        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          zen_einstein
0976a20a1d0f        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          suspicious_jones
e1aa2dbeb05b        ubuntu                            "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        jolly_swirles
be5b8099d8fd        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          practical_fermat
c995d7c5e17e        ubuntu                            "bash"                   2 weeks ago         Exited (130) 2 weeks ago                        jovial_kirch
91761424a8d7        hello-world                       "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                          focused_chatterjee
74bc5baaad36        kartoza/qgis-desktop              "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                          gifted_knuth
5adb571f280a        kartoza/qgis-desktop              "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                          nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker build --pull -t $USER/tensorflow-serving-devel -f ./Dockerfile.devel
"docker build" requires exactly 1 argument.
See 'docker build --help'.

Usage:  docker build [OPTIONS] PATH | URL | - [flags]

Build an image from a Dockerfile
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker build --pull -t $USER/tensorflow-serving-devel -f Dockerfile.devel
"docker build" requires exactly 1 argument.
See 'docker build --help'.

Usage:  docker build [OPTIONS] PATH | URL | - [flags]

Build an image from a Dockerfile
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker build --pull -t $USER/tensorflow-serving-devel -f Dockerfile.devel .
unable to prepare context: unable to evaluate symlinks in Dockerfile path: lstat /media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn/Dockerfile.devel: no such file or directory
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker build --pull -t $USER/tensorflow-serving-devel -f ./Dockerfile.devel .
unable to prepare context: unable to evaluate symlinks in Dockerfile path: lstat /media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn/Dockerfile.devel: no such file or directory
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker build --pull -t $USER/tensorflow-serving-devel -f Dockerfile.devel .
unable to prepare context: unable to evaluate symlinks in Dockerfile path: lstat /media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn/Dockerfile.devel: no such file or directory
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ls
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ls
Dockerfile.devel
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker build --pull -t $USER/tensorflow-serving-devel -f Dockerfile.devel .
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.35/build?buildargs=%7B%7D&cachefrom=%5B%5D&cgroupparent=&cpuperiod=0&cpuquota=0&cpusetcpus=&cpusetmems=&cpushares=0&dockerfile=Dockerfile.devel&labels=%7B%7D&memory=0&memswap=0&networkmode=default&pull=1&rm=1&session=d1f658948d60ebc06adf3c1ba3ff778ed06260fbbf1e217a7bfcfebf7a7bd459&shmsize=0&t=dhankar%2Ftensorflow-serving-devel&target=&ulimits=null: dial unix /var/run/docker.sock: connect: permission denied
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker build --pull -t $USER/tensorflow-serving-devel -f Dockerfile.devel .
Sending build context to Docker daemon  15.87kB
Step 1/9 : FROM ubuntu:16.04
16.04: Pulling from library/ubuntu
Digest: sha256:e348fbbea0e0a0e73ab0370de151e7800684445c509d46195aef73e090a49bd6
Status: Downloaded newer image for ubuntu:16.04
 ---> f975c5035748
Step 2/9 : MAINTAINER Jeremiah Harmsen <jeremiah@google.com>
 ---> Running in 6b4763c7faef
Removing intermediate container 6b4763c7faef
 ---> 50d12acc1a71
Step 3/9 : RUN apt-get update && apt-get install -y         build-essential         curl         git         libfreetype6-dev         libpng12-dev         libzmq3-dev         mlocate         pkg-config         python-dev         python-numpy         python-pip         software-properties-common         swig         zip         zlib1g-dev         libcurl3-dev         openjdk-8-jdk        openjdk-8-jre-headless         wget         &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
 ---> Running in 87cc0b66220d
Get:1 http://security.ubuntu.com/ubuntu xenial-security InRelease [102 kB]
Get:2 http://archive.ubuntu.com/ubuntu xenial InRelease [247 kB]
Get:3 http://security.ubuntu.com/ubuntu xenial-security/universe Sources [77.2 kB]
Get:4 http://security.ubuntu.com/ubuntu xenial-security/main amd64 Packages [601 kB]
Get:5 http://archive.ubuntu.com/ubuntu xenial-updates InRelease [102 kB]
Get:6 http://security.ubuntu.com/ubuntu xenial-security/restricted amd64 Packages [12.7 kB]
Get:7 http://security.ubuntu.com/ubuntu xenial-security/universe amd64 Packages [430 kB]
Get:8 http://archive.ubuntu.com/ubuntu xenial-backports InRelease [102 kB]
Get:9 http://security.ubuntu.com/ubuntu xenial-security/multiverse amd64 Packages [3492 B]
Get:10 http://archive.ubuntu.com/ubuntu xenial/universe Sources [9802 kB]
Get:11 http://archive.ubuntu.com/ubuntu xenial/main amd64 Packages [1558 kB]
Get:12 http://archive.ubuntu.com/ubuntu xenial/restricted amd64 Packages [14.1 kB]
Get:13 http://archive.ubuntu.com/ubuntu xenial/universe amd64 Packages [9827 kB]
Get:14 http://archive.ubuntu.com/ubuntu xenial/multiverse amd64 Packages [176 kB]
Get:15 http://archive.ubuntu.com/ubuntu xenial-updates/universe Sources [250 kB]
Get:16 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 Packages [970 kB]
Get:17 http://archive.ubuntu.com/ubuntu xenial-updates/restricted amd64 Packages [13.1 kB]
Get:18 http://archive.ubuntu.com/ubuntu xenial-updates/universe amd64 Packages [795 kB]
Get:19 http://archive.ubuntu.com/ubuntu xenial-updates/multiverse amd64 Packages [18.5 kB]
Get:20 http://archive.ubuntu.com/ubuntu xenial-backports/main amd64 Packages [5153 B]
Get:21 http://archive.ubuntu.com/ubuntu xenial-backports/universe amd64 Packages [7734 B]
Fetched 25.1 MB in 15s (1602 kB/s)
Reading package lists...
Reading package lists...
Building dependency tree...
Reading state information...
The following additional packages will be installed:
  apt apt-utils binutils bzip2 ca-certificates ca-certificates-java cpp cpp-5
  cron dbus dh-python distro-info-data dpkg-dev fakeroot file fontconfig
  fontconfig-config fonts-dejavu-core fonts-dejavu-extra g++ g++-5 gcc gcc-5
  gir1.2-glib-2.0 git-man hicolor-icon-theme ifupdown iproute2 isc-dhcp-client
  isc-dhcp-common iso-codes java-common krb5-locales less
  libalgorithm-diff-perl libalgorithm-diff-xs-perl libalgorithm-merge-perl
  libapt-inst2.0 libapt-pkg5.0 libasan2 libasn1-8-heimdal libasound2
  libasound2-data libasyncns0 libatk1.0-0 libatk1.0-data libatm1 libatomic1
  libavahi-client3 libavahi-common-data libavahi-common3 libblas-common
  libblas3 libbsd0 libc-dev-bin libc6-dev libcairo2 libcap-ng0 libcc1-0
  libcilkrts5 libcups2 libcurl3 libcurl3-gnutls libdatrie1 libdbus-1-3
  libdbus-glib-1-2 libdns-export162 libdpkg-perl libdrm-amdgpu1 libdrm-common
  libdrm-intel1 libdrm-nouveau2 libdrm-radeon1 libdrm2 libedit2 libelf1
  liberror-perl libexpat1 libexpat1-dev libfakeroot libffi6
  libfile-fcntllock-perl libflac8 libfontconfig1 libfreetype6 libgcc-5-dev
  libgdbm3 libgdk-pixbuf2.0-0 libgdk-pixbuf2.0-common libgfortran3 libgif7
  libgirepository-1.0-1 libgl1-mesa-dri libgl1-mesa-glx libglapi-mesa
  libglib2.0-0 libglib2.0-data libgmp10 libgnutls30 libgomp1 libgraphite2-3
  libgssapi-krb5-2 libgssapi3-heimdal libgtk2.0-0 libgtk2.0-bin
  libgtk2.0-common libharfbuzz0b libhcrypto4-heimdal libheimbase1-heimdal
  libheimntlm0-heimdal libhogweed4 libhx509-5-heimdal libice-dev libice6
  libicu55 libidn11 libisc-export160 libisl15 libitm1 libjbig0 libjpeg-turbo8
  libjpeg8 libjson-c2 libk5crypto3 libkeyutils1 libkrb5-26-heimdal libkrb5-3
  libkrb5support0 liblapack3 liblcms2-2 libldap-2.4-2 libllvm5.0 liblsan0
  libmagic1 libmnl0 libmpc3 libmpdec2 libmpfr4 libmpx0 libnettle6 libnspr4
  libnss3 libnss3-nssdb libogg0 libp11-kit0 libpango-1.0-0 libpangocairo-1.0-0
  libpangoft2-1.0-0 libpciaccess0 libpcsclite1 libperl5.22 libpixman-1-0
  libpng12-0 libpopt0 libpthread-stubs0-dev libpulse0 libpython-all-dev
  libpython-dev libpython-stdlib libpython2.7 libpython2.7-dev
  libpython2.7-minimal libpython2.7-stdlib libpython3-stdlib
  libpython3.5-minimal libpython3.5-stdlib libquadmath0 libroken18-heimdal
  librtmp1 libsasl2-2 libsasl2-modules libsasl2-modules-db libsensors4
  libsm-dev libsm6 libsndfile1 libsodium18 libsqlite3-0 libssl1.0.0
  libstdc++-5-dev libtasn1-6 libthai-data libthai0 libtiff5 libtsan0
  libtxc-dxtn-s2tc0 libubsan0 libvorbis0a libvorbisenc2 libwind0-heimdal
  libwrap0 libx11-6 libx11-data libx11-dev libx11-doc libx11-xcb1 libxau-dev
  libxau6 libxcb-dri2-0 libxcb-dri3-0 libxcb-glx0 libxcb-present0
  libxcb-render0 libxcb-shm0 libxcb-sync1 libxcb1 libxcb1-dev libxcomposite1
  libxcursor1 libxdamage1 libxdmcp-dev libxdmcp6 libxext6 libxfixes3 libxi6
  libxinerama1 libxml2 libxmuu1 libxrandr2 libxrender1 libxshmfence1 libxt-dev
  libxt6 libxtables11 libxtst6 libxxf86vm1 libzmq5 linux-libc-dev lsb-release
  make manpages manpages-dev mime-support netbase openjdk-8-jdk-headless
  openjdk-8-jre openssh-client openssl patch perl perl-modules-5.22 python
  python-all python-all-dev python-apt-common python-minimal python-pip-whl
  python-pkg-resources python-setuptools python-wheel python2.7 python2.7-dev
  python2.7-minimal python3 python3-apt python3-dbus python3-gi
  python3-minimal python3-pycurl python3-software-properties python3.5
  python3.5-minimal rename rsync sgml-base shared-mime-info swig3.0 tcpd ucf
  unattended-upgrades unzip x11-common x11proto-core-dev x11proto-input-dev
  x11proto-kb-dev xauth xdg-user-dirs xml-core xorg-sgml-doctools xtrans-dev
  xz-utils
Suggested packages:
  aptitude | synaptic | wajig apt-doc python-apt binutils-doc bzip2-doc
  cpp-doc gcc-5-locales anacron logrotate checksecurity exim4 | postfix
  | mail-transport-agent dbus-user-session | dbus-x11 debian-keyring
  g++-multilib g++-5-multilib gcc-5-doc libstdc++6-5-dbg gcc-multilib autoconf
  automake libtool flex bison gdb gcc-doc gcc-5-multilib libgcc1-dbg
  libgomp1-dbg libitm1-dbg libatomic1-dbg libasan2-dbg liblsan0-dbg
  libtsan0-dbg libubsan0-dbg libcilkrts5-dbg libmpx0-dbg libquadmath0-dbg
  gettext-base git-daemon-run | git-daemon-sysvinit git-doc git-el git-email
  git-gui gitk gitweb git-arch git-cvs git-mediawiki git-svn ppp rdnssd
  iproute2-doc resolvconf avahi-autoipd isc-dhcp-client-ddns apparmor isoquery
  default-jre libasound2-plugins alsa-utils glibc-doc cups-common libcurl4-doc
  libcurl3-dbg libidn11-dev libkrb5-dev libldap2-dev librtmp-dev libssl-dev
  gnutls-bin krb5-doc krb5-user librsvg2-common gvfs libice-doc liblcms2-utils
  pciutils pcscd pulseaudio libsasl2-modules-otp libsasl2-modules-ldap
  libsasl2-modules-sql libsasl2-modules-gssapi-mit
  | libsasl2-modules-gssapi-heimdal lm-sensors libsm-doc libstdc++-5-doc
  libxcb-doc libxt-doc lsb make-doc man-browser openjdk-8-demo
  openjdk-8-source visualvm icedtea-8-plugin libnss-mdns fonts-ipafont-gothic
  fonts-ipafont-mincho fonts-wqy-microhei fonts-wqy-zenhei fonts-indic
  ssh-askpass libpam-ssh keychain monkeysphere ed diffutils-doc perl-doc
  libterm-readline-gnu-perl | libterm-readline-perl-perl python-doc python-tk
  gfortran python-nose python-numpy-dbg python-numpy-doc python-setuptools-doc
  python2.7-doc binfmt-support python3-doc python3-tk python3-venv
  python3-apt-dbg python-apt-doc python-dbus-doc python3-dbus-dbg
  libcurl4-gnutls-dev python-pycurl-doc python3-pycurl-dbg python3.5-venv
  python3.5-doc openssh-server sgml-base-doc swig-doc swig-examples
  swig3.0-examples swig3.0-doc bsd-mailx mail-transport-agent debhelper
The following NEW packages will be installed:
  apt-utils binutils build-essential bzip2 ca-certificates
  ca-certificates-java cpp cpp-5 cron curl dbus dh-python distro-info-data
  dpkg-dev fakeroot file fontconfig fontconfig-config fonts-dejavu-core
  fonts-dejavu-extra g++ g++-5 gcc gcc-5 gir1.2-glib-2.0 git git-man
  hicolor-icon-theme ifupdown iproute2 isc-dhcp-client isc-dhcp-common
  iso-codes java-common krb5-locales less libalgorithm-diff-perl
  libalgorithm-diff-xs-perl libalgorithm-merge-perl libapt-inst2.0 libasan2
  libasn1-8-heimdal libasound2 libasound2-data libasyncns0 libatk1.0-0
  libatk1.0-data libatm1 libatomic1 libavahi-client3 libavahi-common-data
  libavahi-common3 libblas-common libblas3 libbsd0 libc-dev-bin libc6-dev
  libcairo2 libcap-ng0 libcc1-0 libcilkrts5 libcups2 libcurl3 libcurl3-gnutls
  libcurl4-openssl-dev libdatrie1 libdbus-1-3 libdbus-glib-1-2
  libdns-export162 libdpkg-perl libdrm-amdgpu1 libdrm-common libdrm-intel1
  libdrm-nouveau2 libdrm-radeon1 libdrm2 libedit2 libelf1 liberror-perl
  libexpat1 libexpat1-dev libfakeroot libffi6 libfile-fcntllock-perl libflac8
  libfontconfig1 libfreetype6 libfreetype6-dev libgcc-5-dev libgdbm3
  libgdk-pixbuf2.0-0 libgdk-pixbuf2.0-common libgfortran3 libgif7
  libgirepository-1.0-1 libgl1-mesa-dri libgl1-mesa-glx libglapi-mesa
  libglib2.0-0 libglib2.0-data libgmp10 libgnutls30 libgomp1 libgraphite2-3
  libgssapi-krb5-2 libgssapi3-heimdal libgtk2.0-0 libgtk2.0-bin
  libgtk2.0-common libharfbuzz0b libhcrypto4-heimdal libheimbase1-heimdal
  libheimntlm0-heimdal libhogweed4 libhx509-5-heimdal libice-dev libice6
  libicu55 libidn11 libisc-export160 libisl15 libitm1 libjbig0 libjpeg-turbo8
  libjpeg8 libjson-c2 libk5crypto3 libkeyutils1 libkrb5-26-heimdal libkrb5-3
  libkrb5support0 liblapack3 liblcms2-2 libldap-2.4-2 libllvm5.0 liblsan0
  libmagic1 libmnl0 libmpc3 libmpdec2 libmpfr4 libmpx0 libnettle6 libnspr4
  libnss3 libnss3-nssdb libogg0 libp11-kit0 libpango-1.0-0 libpangocairo-1.0-0
  libpangoft2-1.0-0 libpciaccess0 libpcsclite1 libperl5.22 libpixman-1-0
  libpng12-0 libpng12-dev libpopt0 libpthread-stubs0-dev libpulse0
  libpython-all-dev libpython-dev libpython-stdlib libpython2.7
  libpython2.7-dev libpython2.7-minimal libpython2.7-stdlib libpython3-stdlib
  libpython3.5-minimal libpython3.5-stdlib libquadmath0 libroken18-heimdal
  librtmp1 libsasl2-2 libsasl2-modules libsasl2-modules-db libsensors4
  libsm-dev libsm6 libsndfile1 libsodium18 libsqlite3-0 libssl1.0.0
  libstdc++-5-dev libtasn1-6 libthai-data libthai0 libtiff5 libtsan0
  libtxc-dxtn-s2tc0 libubsan0 libvorbis0a libvorbisenc2 libwind0-heimdal
  libwrap0 libx11-6 libx11-data libx11-dev libx11-doc libx11-xcb1 libxau-dev
  libxau6 libxcb-dri2-0 libxcb-dri3-0 libxcb-glx0 libxcb-present0
  libxcb-render0 libxcb-shm0 libxcb-sync1 libxcb1 libxcb1-dev libxcomposite1
  libxcursor1 libxdamage1 libxdmcp-dev libxdmcp6 libxext6 libxfixes3 libxi6
  libxinerama1 libxml2 libxmuu1 libxrandr2 libxrender1 libxshmfence1 libxt-dev
  libxt6 libxtables11 libxtst6 libxxf86vm1 libzmq3-dev libzmq5 linux-libc-dev
  lsb-release make manpages manpages-dev mime-support mlocate netbase
  openjdk-8-jdk openjdk-8-jdk-headless openjdk-8-jre openjdk-8-jre-headless
  openssh-client openssl patch perl perl-modules-5.22 pkg-config python
  python-all python-all-dev python-apt-common python-dev python-minimal
  python-numpy python-pip python-pip-whl python-pkg-resources
  python-setuptools python-wheel python2.7 python2.7-dev python2.7-minimal
  python3 python3-apt python3-dbus python3-gi python3-minimal python3-pycurl
  python3-software-properties python3.5 python3.5-minimal rename rsync
  sgml-base shared-mime-info software-properties-common swig swig3.0 tcpd ucf
  unattended-upgrades unzip wget x11-common x11proto-core-dev
  x11proto-input-dev x11proto-kb-dev xauth xdg-user-dirs xml-core
  xorg-sgml-doctools xtrans-dev xz-utils zip zlib1g-dev
The following packages will be upgraded:
  apt libapt-pkg5.0
2 upgraded, 298 newly installed, 0 to remove and 7 not upgraded.
Need to get 192 MB of archives.
After this operation, 826 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libapt-pkg5.0 amd64 1.2.26 [706 kB]
Get:2 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 apt amd64 1.2.26 [1043 kB]
Get:3 http://archive.ubuntu.com/ubuntu xenial/main amd64 cron amd64 3.0pl1-128ubuntu2 [68.4 kB]
Get:4 http://archive.ubuntu.com/ubuntu xenial/main amd64 libatm1 amd64 1:2.5.1-1.5 [24.2 kB]
Get:5 http://archive.ubuntu.com/ubuntu xenial/main amd64 libjson-c2 amd64 0.11-4ubuntu2 [22.3 kB]
Get:6 http://archive.ubuntu.com/ubuntu xenial/main amd64 libmnl0 amd64 1.0.3-5 [12.0 kB]
Get:7 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpopt0 amd64 1.16-10 [26.0 kB]
Get:8 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libssl1.0.0 amd64 1.0.2g-1ubuntu4.11 [1082 kB]
Get:9 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython3.5-minimal amd64 3.5.2-2ubuntu0~16.04.4 [523 kB]
Get:10 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libexpat1 amd64 2.1.0-7ubuntu0.16.04.3 [71.2 kB]
Get:11 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python3.5-minimal amd64 3.5.2-2ubuntu0~16.04.4 [1597 kB]
Get:12 http://archive.ubuntu.com/ubuntu xenial/main amd64 python3-minimal amd64 3.5.1-3 [23.3 kB]
Get:13 http://archive.ubuntu.com/ubuntu xenial/main amd64 mime-support all 3.59ubuntu1 [31.0 kB]
Get:14 http://archive.ubuntu.com/ubuntu xenial/main amd64 libmpdec2 amd64 2.4.2-1 [82.6 kB]
Get:15 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsqlite3-0 amd64 3.11.0-1ubuntu1 [396 kB]
Get:16 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython3.5-stdlib amd64 3.5.2-2ubuntu0~16.04.4 [2132 kB]
Get:17 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python3.5 amd64 3.5.2-2ubuntu0~16.04.4 [165 kB]
Get:18 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpython3-stdlib amd64 3.5.1-3 [6818 B]
Get:19 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 dh-python all 2.20151103ubuntu1.1 [74.1 kB]
Get:20 http://archive.ubuntu.com/ubuntu xenial/main amd64 python3 amd64 3.5.1-3 [8710 B]
Get:21 http://archive.ubuntu.com/ubuntu xenial/main amd64 libgdbm3 amd64 1.8.3-13.1 [16.9 kB]
Get:22 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxau6 amd64 1:1.0.8-1 [8376 B]
Get:23 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxdmcp6 amd64 1:1.1.2-1.1 [11.0 kB]
Get:24 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb1 amd64 1.11.1-1ubuntu1 [40.0 kB]
Get:25 http://archive.ubuntu.com/ubuntu xenial/main amd64 libx11-data all 2:1.6.3-1ubuntu2 [113 kB]
Get:26 http://archive.ubuntu.com/ubuntu xenial/main amd64 libx11-6 amd64 2:1.6.3-1ubuntu2 [571 kB]
Get:27 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxext6 amd64 2:1.3.3-1 [29.4 kB]
Get:28 http://archive.ubuntu.com/ubuntu xenial/main amd64 sgml-base all 1.26+nmu4ubuntu1 [12.5 kB]
Get:29 http://archive.ubuntu.com/ubuntu xenial/main amd64 fonts-dejavu-core all 2.35-1 [1039 kB]
Get:30 http://archive.ubuntu.com/ubuntu xenial/main amd64 ucf all 3.0036 [52.9 kB]
Get:31 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 fontconfig-config all 2.11.94-0ubuntu1.1 [49.9 kB]
Get:32 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpng12-0 amd64 1.2.54-1ubuntu1 [116 kB]
Get:33 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libfreetype6 amd64 2.6.1-0.1ubuntu2.3 [316 kB]
Get:34 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libfontconfig1 amd64 2.11.94-0ubuntu1.1 [131 kB]
Get:35 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 fontconfig amd64 2.11.94-0ubuntu1.1 [178 kB]
Get:36 http://archive.ubuntu.com/ubuntu xenial/main amd64 libasyncns0 amd64 0.8-5build1 [12.3 kB]
Get:37 http://archive.ubuntu.com/ubuntu xenial/main amd64 x11-common all 1:7.7+13ubuntu3 [22.4 kB]
Get:38 http://archive.ubuntu.com/ubuntu xenial/main amd64 libice6 amd64 2:1.0.9-1 [39.2 kB]
Get:39 http://archive.ubuntu.com/ubuntu xenial/main amd64 libjpeg-turbo8 amd64 1.4.2-0ubuntu3 [111 kB]
Get:40 http://archive.ubuntu.com/ubuntu xenial/main amd64 liblcms2-2 amd64 2.6-3ubuntu2 [137 kB]
Get:41 http://archive.ubuntu.com/ubuntu xenial/main amd64 libogg0 amd64 1.3.2-1 [17.2 kB]
Get:42 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsm6 amd64 2:1.2.2-1 [15.8 kB]
Get:43 http://archive.ubuntu.com/ubuntu xenial/main amd64 libwrap0 amd64 7.6.q-25 [46.2 kB]
Get:44 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcomposite1 amd64 1:0.4.4-1 [7714 B]
Get:45 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxdamage1 amd64 1:1.1.4-2 [6946 B]
Get:46 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxfixes3 amd64 1:5.0.1-2 [11.1 kB]
Get:47 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxinerama1 amd64 2:1.1.3-1 [7908 B]
Get:48 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxshmfence1 amd64 1.2-1 [5042 B]
Get:49 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxtst6 amd64 2:1.2.2-1 [14.1 kB]
Get:50 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxxf86vm1 amd64 1:1.1.4-1 [10.6 kB]
Get:51 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 perl-modules-5.22 all 5.22.1-9ubuntu0.2 [2661 kB]
Get:52 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libperl5.22 amd64 5.22.1-9ubuntu0.2 [3391 kB]
Get:53 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 perl amd64 5.22.1-9ubuntu0.2 [237 kB]
Get:54 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython2.7-minimal amd64 2.7.12-1ubuntu0~16.04.3 [340 kB]
Get:55 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python2.7-minimal amd64 2.7.12-1ubuntu0~16.04.3 [1261 kB]
Get:56 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python-minimal amd64 2.7.12-1~16.04 [28.1 kB]
Get:57 http://archive.ubuntu.com/ubuntu xenial/main amd64 libffi6 amd64 3.2.1-4 [17.8 kB]
Get:58 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython2.7-stdlib amd64 2.7.12-1ubuntu0~16.04.3 [1880 kB]
Get:59 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python2.7 amd64 2.7.12-1ubuntu0~16.04.3 [224 kB]
Get:60 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython-stdlib amd64 2.7.12-1~16.04 [7768 B]
Get:61 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python amd64 2.7.12-1~16.04 [137 kB]
Get:62 http://archive.ubuntu.com/ubuntu xenial/main amd64 libjbig0 amd64 2.1-3.1 [26.6 kB]
Get:63 http://archive.ubuntu.com/ubuntu xenial/main amd64 libgmp10 amd64 2:6.1.0+dfsg-2 [240 kB]
Get:64 http://archive.ubuntu.com/ubuntu xenial/main amd64 libmpfr4 amd64 3.1.4-1 [191 kB]
Get:65 http://archive.ubuntu.com/ubuntu xenial/main amd64 libmpc3 amd64 1.0.3-1 [39.7 kB]
Get:66 http://archive.ubuntu.com/ubuntu xenial/main amd64 libtxc-dxtn-s2tc0 amd64 0~git20131104-1.1 [51.8 kB]
Get:67 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libapt-inst2.0 amd64 1.2.26 [55.4 kB]
Get:68 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 apt-utils amd64 1.2.26 [197 kB]
Get:69 http://archive.ubuntu.com/ubuntu xenial/main amd64 bzip2 amd64 1.0.6-8 [32.7 kB]
Get:70 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 distro-info-data all 0.28ubuntu0.7 [4334 B]
Get:71 http://archive.ubuntu.com/ubuntu xenial/main amd64 libmagic1 amd64 1:5.25-2ubuntu1 [216 kB]
Get:72 http://archive.ubuntu.com/ubuntu xenial/main amd64 file amd64 1:5.25-2ubuntu1 [21.2 kB]
Get:73 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 iproute2 amd64 4.3.0-1ubuntu3.16.04.3 [522 kB]
Get:74 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 ifupdown amd64 0.8.10ubuntu1.2 [54.9 kB]
Get:75 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libisc-export160 amd64 1:9.10.3.dfsg.P4-8ubuntu1.10 [153 kB]
Get:76 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdns-export162 amd64 1:9.10.3.dfsg.P4-8ubuntu1.10 [666 kB]
Get:77 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 isc-dhcp-client amd64 4.3.3-5ubuntu12.10 [224 kB]
Get:78 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 isc-dhcp-common amd64 4.3.3-5ubuntu12.10 [105 kB]
Get:79 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 less amd64 481-2.1ubuntu0.2 [110 kB]
Get:80 http://archive.ubuntu.com/ubuntu xenial/main amd64 libbsd0 amd64 0.8.2-1 [41.7 kB]
Get:81 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libnettle6 amd64 3.2-1ubuntu0.16.04.1 [93.5 kB]
Get:82 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libhogweed4 amd64 3.2-1ubuntu0.16.04.1 [136 kB]
Get:83 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libidn11 amd64 1.32-3ubuntu1.2 [46.5 kB]
Get:84 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libp11-kit0 amd64 0.23.2-5~ubuntu16.04.1 [105 kB]
Get:85 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libtasn1-6 amd64 4.7-3ubuntu0.16.04.3 [43.5 kB]
Get:86 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgnutls30 amd64 3.4.10-4ubuntu1.4 [548 kB]
Get:87 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxtables11 amd64 1.6.0-2ubuntu3 [27.2 kB]
Get:88 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 lsb-release all 9.20160110ubuntu0.2 [11.8 kB]
Get:89 http://archive.ubuntu.com/ubuntu xenial/main amd64 netbase all 5.3 [12.9 kB]
Get:90 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 openssl amd64 1.0.2g-1ubuntu4.11 [492 kB]
Get:91 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 ca-certificates all 20170717~16.04.1 [168 kB]
Get:92 http://archive.ubuntu.com/ubuntu xenial/main amd64 libcap-ng0 amd64 0.7.7-1 [10.9 kB]
Get:93 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdbus-1-3 amd64 1.10.6-1ubuntu3.3 [161 kB]
Get:94 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 dbus amd64 1.10.6-1ubuntu3.3 [142 kB]
Get:95 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libglib2.0-0 amd64 2.48.2-0ubuntu1 [1119 kB]
Get:96 http://archive.ubuntu.com/ubuntu xenial/main amd64 libgirepository-1.0-1 amd64 1.46.0-3ubuntu1 [88.3 kB]
Get:97 http://archive.ubuntu.com/ubuntu xenial/main amd64 gir1.2-glib-2.0 amd64 1.46.0-3ubuntu1 [127 kB]
Get:98 http://archive.ubuntu.com/ubuntu xenial/main amd64 iso-codes all 3.65-1 [2268 kB]
Get:99 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 krb5-locales all 1.13.2+dfsg-5ubuntu2 [13.2 kB]
Get:100 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libroken18-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [41.4 kB]
Get:101 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libasn1-8-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [174 kB]
Get:102 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libkrb5support0 amd64 1.13.2+dfsg-5ubuntu2 [30.8 kB]
Get:103 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libk5crypto3 amd64 1.13.2+dfsg-5ubuntu2 [81.2 kB]
Get:104 http://archive.ubuntu.com/ubuntu xenial/main amd64 libkeyutils1 amd64 1.5.9-8ubuntu1 [9904 B]
Get:105 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libkrb5-3 amd64 1.13.2+dfsg-5ubuntu2 [273 kB]
Get:106 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgssapi-krb5-2 amd64 1.13.2+dfsg-5ubuntu2 [120 kB]
Get:107 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libhcrypto4-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [85.0 kB]
Get:108 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libheimbase1-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [29.3 kB]
Get:109 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libwind0-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [47.8 kB]
Get:110 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libhx509-5-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [107 kB]
Get:111 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libkrb5-26-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [202 kB]
Get:112 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libheimntlm0-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [15.1 kB]
Get:113 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgssapi3-heimdal amd64 1.7~git20150920+dfsg-4ubuntu1.16.04.1 [96.1 kB]
Get:114 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsasl2-modules-db amd64 2.1.26.dfsg1-14build1 [14.5 kB]
Get:115 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsasl2-2 amd64 2.1.26.dfsg1-14build1 [48.7 kB]
Get:116 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libldap-2.4-2 amd64 2.4.42+dfsg-2ubuntu3.2 [160 kB]
Get:117 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 librtmp1 amd64 2.4+20151223.gitfa8646d-1ubuntu0.1 [54.4 kB]
Get:118 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libcurl3-gnutls amd64 7.47.0-1ubuntu2.7 [185 kB]
Get:119 http://archive.ubuntu.com/ubuntu xenial/main amd64 libdbus-glib-1-2 amd64 0.106-1 [67.1 kB]
Get:120 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdrm-common all 2.4.83-1~16.04.1 [4870 B]
Get:121 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdrm2 amd64 2.4.83-1~16.04.1 [30.4 kB]
Get:122 http://archive.ubuntu.com/ubuntu xenial/main amd64 libedit2 amd64 3.1-20150325-1ubuntu2 [76.5 kB]
Get:123 http://archive.ubuntu.com/ubuntu xenial/main amd64 libelf1 amd64 0.165-3ubuntu1 [42.5 kB]
Get:124 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libglib2.0-data all 2.48.2-0ubuntu1 [132 kB]
Get:125 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libicu55 amd64 55.1-7ubuntu0.4 [7646 kB]
Get:126 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsasl2-modules amd64 2.1.26.dfsg1-14build1 [47.5 kB]
Get:127 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libxml2 amd64 2.9.3+dfsg1-1ubuntu0.5 [697 kB]
Get:128 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxmuu1 amd64 2:1.1.2-2 [9674 B]
Get:129 http://archive.ubuntu.com/ubuntu xenial/main amd64 manpages all 4.04-2 [1087 kB]
Get:130 http://archive.ubuntu.com/ubuntu xenial/main amd64 mlocate amd64 0.26-1ubuntu2 [45.4 kB]
Get:131 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 openssh-client amd64 1:7.2p2-4ubuntu2.4 [589 kB]
Get:132 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python-apt-common all 1.1.0~beta1ubuntu0.16.04.1 [16.0 kB]
Get:133 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python3-apt amd64 1.1.0~beta1ubuntu0.16.04.1 [137 kB]
Get:134 http://archive.ubuntu.com/ubuntu xenial/main amd64 python3-dbus amd64 1.2.0-3 [83.1 kB]
Get:135 http://archive.ubuntu.com/ubuntu xenial/main amd64 python3-gi amd64 3.20.0-0ubuntu1 [153 kB]
Get:136 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 rsync amd64 3.1.1-3ubuntu1.2 [329 kB]
Get:137 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 shared-mime-info amd64 1.5-2ubuntu0.1 [405 kB]
Get:138 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 wget amd64 1.17.1-1ubuntu1.3 [299 kB]
Get:139 http://archive.ubuntu.com/ubuntu xenial/main amd64 xauth amd64 1:1.0.9-1ubuntu2 [22.7 kB]
Get:140 http://archive.ubuntu.com/ubuntu xenial/main amd64 xdg-user-dirs amd64 0.15-2ubuntu6 [61.7 kB]
Get:141 http://archive.ubuntu.com/ubuntu xenial/main amd64 xml-core all 0.13+nmu2 [23.3 kB]
Get:142 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 binutils amd64 2.26.1-1ubuntu1~16.04.6 [2311 kB]
Get:143 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libc-dev-bin amd64 2.23-0ubuntu10 [68.7 kB]
Get:144 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 linux-libc-dev amd64 4.4.0-119.143 [845 kB]
Get:145 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libc6-dev amd64 2.23-0ubuntu10 [2079 kB]
Get:146 http://archive.ubuntu.com/ubuntu xenial/main amd64 libisl15 amd64 0.16.1-1 [524 kB]
Get:147 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 cpp-5 amd64 5.4.0-6ubuntu1~16.04.9 [7685 kB]
Get:148 http://archive.ubuntu.com/ubuntu xenial/main amd64 cpp amd64 4:5.3.1-1ubuntu1 [27.7 kB]
Get:149 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libcc1-0 amd64 5.4.0-6ubuntu1~16.04.9 [38.8 kB]
Get:150 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgomp1 amd64 5.4.0-6ubuntu1~16.04.9 [55.0 kB]
Get:151 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libitm1 amd64 5.4.0-6ubuntu1~16.04.9 [27.4 kB]
Get:152 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libatomic1 amd64 5.4.0-6ubuntu1~16.04.9 [8882 B]
Get:153 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libasan2 amd64 5.4.0-6ubuntu1~16.04.9 [264 kB]
Get:154 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 liblsan0 amd64 5.4.0-6ubuntu1~16.04.9 [105 kB]
Get:155 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libtsan0 amd64 5.4.0-6ubuntu1~16.04.9 [244 kB]
Get:156 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libubsan0 amd64 5.4.0-6ubuntu1~16.04.9 [95.2 kB]
Get:157 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libcilkrts5 amd64 5.4.0-6ubuntu1~16.04.9 [40.1 kB]
Get:158 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libmpx0 amd64 5.4.0-6ubuntu1~16.04.9 [9774 B]
Get:159 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libquadmath0 amd64 5.4.0-6ubuntu1~16.04.9 [131 kB]
Get:160 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgcc-5-dev amd64 5.4.0-6ubuntu1~16.04.9 [2242 kB]
Get:161 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 gcc-5 amd64 5.4.0-6ubuntu1~16.04.9 [8650 kB]
Get:162 http://archive.ubuntu.com/ubuntu xenial/main amd64 gcc amd64 4:5.3.1-1ubuntu1 [5244 B]
Get:163 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libstdc++-5-dev amd64 5.4.0-6ubuntu1~16.04.9 [1427 kB]
Get:164 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 g++-5 amd64 5.4.0-6ubuntu1~16.04.9 [8333 kB]
Get:165 http://archive.ubuntu.com/ubuntu xenial/main amd64 g++ amd64 4:5.3.1-1ubuntu1 [1504 B]
Get:166 http://archive.ubuntu.com/ubuntu xenial/main amd64 make amd64 4.1-6 [151 kB]
Get:167 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdpkg-perl all 1.18.4ubuntu1.4 [195 kB]
Get:168 http://archive.ubuntu.com/ubuntu xenial/main amd64 xz-utils amd64 5.1.1alpha+20120614-2ubuntu2 [78.8 kB]
Get:169 http://archive.ubuntu.com/ubuntu xenial/main amd64 patch amd64 2.7.5-1 [90.4 kB]
Get:170 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 dpkg-dev all 1.18.4ubuntu1.4 [584 kB]
Get:171 http://archive.ubuntu.com/ubuntu xenial/main amd64 build-essential amd64 12.1ubuntu2 [4758 B]
Get:172 http://archive.ubuntu.com/ubuntu xenial/main amd64 java-common all 0.56ubuntu2 [7742 B]
Get:173 http://archive.ubuntu.com/ubuntu xenial/main amd64 libavahi-common-data amd64 0.6.32~rc+dfsg-1ubuntu2 [21.7 kB]
Get:174 http://archive.ubuntu.com/ubuntu xenial/main amd64 libavahi-common3 amd64 0.6.32~rc+dfsg-1ubuntu2 [21.6 kB]
Get:175 http://archive.ubuntu.com/ubuntu xenial/main amd64 libavahi-client3 amd64 0.6.32~rc+dfsg-1ubuntu2 [25.1 kB]
Get:176 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libcups2 amd64 2.1.3-4ubuntu0.4 [197 kB]
Get:177 http://archive.ubuntu.com/ubuntu xenial/main amd64 libjpeg8 amd64 8c-2ubuntu8 [2194 B]
Get:178 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libnspr4 amd64 2:4.13.1-0ubuntu0.16.04.1 [112 kB]
Get:179 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libnss3-nssdb all 2:3.28.4-0ubuntu0.16.04.3 [10.6 kB]
Get:180 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libnss3 amd64 2:3.28.4-0ubuntu0.16.04.3 [1148 kB]
Get:181 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpcsclite1 amd64 1.8.14-1ubuntu1.16.04.1 [21.4 kB]
Get:182 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxi6 amd64 2:1.7.6-1 [28.6 kB]
Get:183 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxrender1 amd64 1:0.9.9-0ubuntu1 [18.5 kB]
Get:184 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 openjdk-8-jre-headless amd64 8u162-b12-0ubuntu0.16.04.2 [27.0 MB]
Get:185 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 ca-certificates-java all 20160321ubuntu1 [12.5 kB]
Get:186 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 curl amd64 7.47.0-1ubuntu2.7 [138 kB]
Get:187 http://archive.ubuntu.com/ubuntu xenial/main amd64 libfakeroot amd64 1.20.2-1ubuntu1 [25.5 kB]
Get:188 http://archive.ubuntu.com/ubuntu xenial/main amd64 fakeroot amd64 1.20.2-1ubuntu1 [61.8 kB]
Get:189 http://archive.ubuntu.com/ubuntu xenial/main amd64 fonts-dejavu-extra all 2.35-1 [1749 kB]
Get:190 http://archive.ubuntu.com/ubuntu xenial/main amd64 liberror-perl all 0.17-1.2 [19.6 kB]
Get:191 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 git-man all 1:2.7.4-0ubuntu1.3 [736 kB]
Get:192 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 git amd64 1:2.7.4-0ubuntu1.3 [3102 kB]
Get:193 http://archive.ubuntu.com/ubuntu xenial/main amd64 hicolor-icon-theme all 0.15-0ubuntu1 [7750 B]
Get:194 http://archive.ubuntu.com/ubuntu xenial/main amd64 libalgorithm-diff-perl all 1.19.03-1 [47.6 kB]
Get:195 http://archive.ubuntu.com/ubuntu xenial/main amd64 libalgorithm-diff-xs-perl amd64 0.04-4build1 [11.0 kB]
Get:196 http://archive.ubuntu.com/ubuntu xenial/main amd64 libalgorithm-merge-perl all 0.08-3 [12.0 kB]
Get:197 http://archive.ubuntu.com/ubuntu xenial/main amd64 libasound2-data all 1.1.0-0ubuntu1 [29.4 kB]
Get:198 http://archive.ubuntu.com/ubuntu xenial/main amd64 libasound2 amd64 1.1.0-0ubuntu1 [350 kB]
Get:199 http://archive.ubuntu.com/ubuntu xenial/main amd64 libatk1.0-data all 2.18.0-1 [17.1 kB]
Get:200 http://archive.ubuntu.com/ubuntu xenial/main amd64 libatk1.0-0 amd64 2.18.0-1 [56.9 kB]
Get:201 http://archive.ubuntu.com/ubuntu xenial/main amd64 libblas-common amd64 3.6.0-2ubuntu2 [5342 B]
Get:202 http://archive.ubuntu.com/ubuntu xenial/main amd64 libblas3 amd64 3.6.0-2ubuntu2 [147 kB]
Get:203 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpixman-1-0 amd64 0.33.6-1 [231 kB]
Get:204 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-render0 amd64 1.11.1-1ubuntu1 [11.4 kB]
Get:205 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-shm0 amd64 1.11.1-1ubuntu1 [5588 B]
Get:206 http://archive.ubuntu.com/ubuntu xenial/main amd64 libcairo2 amd64 1.14.6-1 [555 kB]
Get:207 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libcurl3 amd64 7.47.0-1ubuntu2.7 [187 kB]
Get:208 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libcurl4-openssl-dev amd64 7.47.0-1ubuntu2.7 [262 kB]
Get:209 http://archive.ubuntu.com/ubuntu xenial/main amd64 libdatrie1 amd64 0.2.10-2 [17.3 kB]
Get:210 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdrm-amdgpu1 amd64 2.4.83-1~16.04.1 [18.6 kB]
Get:211 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpciaccess0 amd64 0.13.4-1 [18.1 kB]
Get:212 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdrm-intel1 amd64 2.4.83-1~16.04.1 [59.9 kB]
Get:213 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdrm-nouveau2 amd64 2.4.83-1~16.04.1 [16.3 kB]
Get:214 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libdrm-radeon1 amd64 2.4.83-1~16.04.1 [21.5 kB]
Get:215 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libexpat1-dev amd64 2.1.0-7ubuntu0.16.04.3 [115 kB]
Get:216 http://archive.ubuntu.com/ubuntu xenial/main amd64 libfile-fcntllock-perl amd64 0.22-3 [32.0 kB]
Get:217 http://archive.ubuntu.com/ubuntu xenial/main amd64 libflac8 amd64 1.3.1-4 [210 kB]
Get:218 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 zlib1g-dev amd64 1:1.2.8.dfsg-2ubuntu4.1 [168 kB]
Get:219 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpng12-dev amd64 1.2.54-1ubuntu1 [184 kB]
Get:220 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libfreetype6-dev amd64 2.6.1-0.1ubuntu2.3 [956 kB]
Get:221 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libtiff5 amd64 4.0.6-1ubuntu0.4 [148 kB]
Get:222 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgdk-pixbuf2.0-common all 2.32.2-1ubuntu1.4 [10.5 kB]
Get:223 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgdk-pixbuf2.0-0 amd64 2.32.2-1ubuntu1.4 [158 kB]
Get:224 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgfortran3 amd64 5.4.0-6ubuntu1~16.04.9 [260 kB]
Get:225 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgif7 amd64 5.1.4-0.3~16.04 [30.5 kB]
Get:226 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libglapi-mesa amd64 17.2.8-0ubuntu0~16.04.1 [22.8 kB]
Get:227 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libllvm5.0 amd64 1:5.0-3~16.04.1 [13.5 MB]
Get:228 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsensors4 amd64 1:3.4.0-2 [28.4 kB]
Get:229 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgl1-mesa-dri amd64 17.2.8-0ubuntu0~16.04.1 [5782 kB]
Get:230 http://archive.ubuntu.com/ubuntu xenial/main amd64 libx11-xcb1 amd64 2:1.6.3-1ubuntu2 [8956 B]
Get:231 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-dri2-0 amd64 1.11.1-1ubuntu1 [6882 B]
Get:232 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-dri3-0 amd64 1.11.1-1ubuntu1 [5218 B]
Get:233 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-glx0 amd64 1.11.1-1ubuntu1 [20.9 kB]
Get:234 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-present0 amd64 1.11.1-1ubuntu1 [5218 B]
Get:235 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb-sync1 amd64 1.11.1-1ubuntu1 [8324 B]
Get:236 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgl1-mesa-glx amd64 17.2.8-0ubuntu0~16.04.1 [130 kB]
Get:237 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgraphite2-3 amd64 1.3.10-0ubuntu0.16.04.1 [71.7 kB]
Get:238 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgtk2.0-common all 2.24.30-1ubuntu1.16.04.2 [123 kB]
Get:239 http://archive.ubuntu.com/ubuntu xenial/main amd64 libthai-data all 0.1.24-2 [131 kB]
Get:240 http://archive.ubuntu.com/ubuntu xenial/main amd64 libthai0 amd64 0.1.24-2 [17.3 kB]
Get:241 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpango-1.0-0 amd64 1.38.1-1 [148 kB]
Get:242 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libharfbuzz0b amd64 1.0.1-1ubuntu0.1 [140 kB]
Get:243 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpangoft2-1.0-0 amd64 1.38.1-1 [33.3 kB]
Get:244 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpangocairo-1.0-0 amd64 1.38.1-1 [20.5 kB]
Get:245 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libxcursor1 amd64 1:1.1.14-1ubuntu0.16.04.1 [20.2 kB]
Get:246 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxrandr2 amd64 2:1.5.0-1 [17.6 kB]
Get:247 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgtk2.0-0 amd64 2.24.30-1ubuntu1.16.04.2 [1775 kB]
Get:248 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgtk2.0-bin amd64 2.24.30-1ubuntu1.16.04.2 [9834 B]
Get:249 http://archive.ubuntu.com/ubuntu xenial/main amd64 xorg-sgml-doctools all 1:1.11-1 [12.9 kB]
Get:250 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 x11proto-core-dev all 7.0.31-1~ubuntu16.04.2 [254 kB]
Get:251 http://archive.ubuntu.com/ubuntu xenial/main amd64 libice-dev amd64 2:1.0.9-1 [44.9 kB]
Get:252 http://archive.ubuntu.com/ubuntu xenial/main amd64 liblapack3 amd64 3.6.0-2ubuntu2 [1938 kB]
Get:253 http://archive.ubuntu.com/ubuntu xenial/main amd64 libpthread-stubs0-dev amd64 0.3-4 [4068 B]
Get:254 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libvorbis0a amd64 1.3.5-3ubuntu0.2 [86.0 kB]
Get:255 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libvorbisenc2 amd64 1.3.5-3ubuntu0.2 [70.6 kB]
Get:256 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libsndfile1 amd64 1.0.25-10ubuntu0.16.04.1 [138 kB]
Get:257 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpulse0 amd64 1:8.0-0ubuntu3.8 [249 kB]
Get:258 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython2.7 amd64 2.7.12-1ubuntu0~16.04.3 [1070 kB]
Get:259 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython2.7-dev amd64 2.7.12-1ubuntu0~16.04.3 [27.8 MB]
Get:260 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython-dev amd64 2.7.12-1~16.04 [7840 B]
Get:261 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 libpython-all-dev amd64 2.7.12-1~16.04 [1006 B]
Get:262 http://archive.ubuntu.com/ubuntu xenial/main amd64 libsm-dev amd64 2:1.2.2-1 [16.2 kB]
Get:263 http://archive.ubuntu.com/ubuntu xenial/universe amd64 libsodium18 amd64 1.0.8-5 [144 kB]
Get:264 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxau-dev amd64 1:1.0.8-1 [11.1 kB]
Get:265 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxdmcp-dev amd64 1:1.1.2-1.1 [25.1 kB]
Get:266 http://archive.ubuntu.com/ubuntu xenial/main amd64 x11proto-input-dev all 2.3.1-1 [118 kB]
Get:267 http://archive.ubuntu.com/ubuntu xenial/main amd64 x11proto-kb-dev all 1.0.7-0ubuntu1 [224 kB]
Get:268 http://archive.ubuntu.com/ubuntu xenial/main amd64 xtrans-dev all 1.3.5-1 [70.5 kB]
Get:269 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxcb1-dev amd64 1.11.1-1ubuntu1 [74.2 kB]
Get:270 http://archive.ubuntu.com/ubuntu xenial/main amd64 libx11-dev amd64 2:1.6.3-1ubuntu2 [642 kB]
Get:271 http://archive.ubuntu.com/ubuntu xenial/main amd64 libx11-doc all 2:1.6.3-1ubuntu2 [1465 kB]
Get:272 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxt6 amd64 1:1.1.5-0ubuntu1 [160 kB]
Get:273 http://archive.ubuntu.com/ubuntu xenial/main amd64 libxt-dev amd64 1:1.1.5-0ubuntu1 [394 kB]
Get:274 http://archive.ubuntu.com/ubuntu xenial/universe amd64 libzmq5 amd64 4.1.4-7 [149 kB]
Get:275 http://archive.ubuntu.com/ubuntu xenial/universe amd64 libzmq3-dev amd64 4.1.4-7 [282 kB]
Get:276 http://archive.ubuntu.com/ubuntu xenial/main amd64 manpages-dev all 4.04-2 [2048 kB]
Get:277 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 openjdk-8-jre amd64 8u162-b12-0ubuntu0.16.04.2 [69.4 kB]
Get:278 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 openjdk-8-jdk-headless amd64 8u162-b12-0ubuntu0.16.04.2 [8212 kB]
Get:279 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 openjdk-8-jdk amd64 8u162-b12-0ubuntu0.16.04.2 [452 kB]
Get:280 http://archive.ubuntu.com/ubuntu xenial/main amd64 pkg-config amd64 0.29.1-0ubuntu1 [45.0 kB]
Get:281 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python-all amd64 2.7.12-1~16.04 [996 B]
Get:282 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python2.7-dev amd64 2.7.12-1ubuntu0~16.04.3 [276 kB]
Get:283 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python-dev amd64 2.7.12-1~16.04 [1186 B]
Get:284 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python-all-dev amd64 2.7.12-1~16.04 [1016 B]
Get:285 http://archive.ubuntu.com/ubuntu xenial/main amd64 python-numpy amd64 1:1.11.0-1ubuntu1 [1763 kB]
Get:286 http://archive.ubuntu.com/ubuntu xenial-updates/universe amd64 python-pip-whl all 8.1.1-2ubuntu0.4 [1110 kB]
Get:287 http://archive.ubuntu.com/ubuntu xenial-updates/universe amd64 python-pip all 8.1.1-2ubuntu0.4 [144 kB]
Get:288 http://archive.ubuntu.com/ubuntu xenial/main amd64 python-pkg-resources all 20.7.0-1 [108 kB]
Get:289 http://archive.ubuntu.com/ubuntu xenial/main amd64 python-setuptools all 20.7.0-1 [169 kB]
Get:290 http://archive.ubuntu.com/ubuntu xenial/universe amd64 python-wheel all 0.29.0-1 [48.0 kB]
Get:291 http://archive.ubuntu.com/ubuntu xenial/main amd64 python3-pycurl amd64 7.43.0-1ubuntu1 [42.3 kB]
Get:292 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 python3-software-properties all 0.96.20.7 [20.3 kB]
Get:293 http://archive.ubuntu.com/ubuntu xenial/main amd64 rename all 0.20-4 [12.0 kB]
Get:294 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 software-properties-common all 0.96.20.7 [9452 B]
Get:295 http://archive.ubuntu.com/ubuntu xenial/universe amd64 swig3.0 amd64 3.0.8-0ubuntu3 [995 kB]
Get:296 http://archive.ubuntu.com/ubuntu xenial/universe amd64 swig amd64 3.0.8-0ubuntu3 [6278 B]
Get:297 http://archive.ubuntu.com/ubuntu xenial/main amd64 tcpd amd64 7.6.q-25 [23.0 kB]
Get:298 http://archive.ubuntu.com/ubuntu xenial-updates/main amd64 unattended-upgrades all 0.90ubuntu0.9 [32.3 kB]
Get:299 http://archive.ubuntu.com/ubuntu xenial/main amd64 unzip amd64 6.0-20ubuntu1 [158 kB]
Get:300 http://archive.ubuntu.com/ubuntu xenial/main amd64 zip amd64 3.0-11 [158 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 192 MB in 2min 8s (1498 kB/s)
(Reading database ... 4768 files and directories currently installed.)
Preparing to unpack .../libapt-pkg5.0_1.2.26_amd64.deb ...
Unpacking libapt-pkg5.0:amd64 (1.2.26) over (1.2.25) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Setting up libapt-pkg5.0:amd64 (1.2.26) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
(Reading database ... 4768 files and directories currently installed.)
Preparing to unpack .../archives/apt_1.2.26_amd64.deb ...
Unpacking apt (1.2.26) over (1.2.25) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Setting up apt (1.2.26) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Selecting previously unselected package cron.
(Reading database ... 4768 files and directories currently installed.)
Preparing to unpack .../cron_3.0pl1-128ubuntu2_amd64.deb ...
Unpacking cron (3.0pl1-128ubuntu2) ...
Selecting previously unselected package libatm1:amd64.
Preparing to unpack .../libatm1_1%3a2.5.1-1.5_amd64.deb ...
Unpacking libatm1:amd64 (1:2.5.1-1.5) ...
Selecting previously unselected package libjson-c2:amd64.
Preparing to unpack .../libjson-c2_0.11-4ubuntu2_amd64.deb ...
Unpacking libjson-c2:amd64 (0.11-4ubuntu2) ...
Selecting previously unselected package libmnl0:amd64.
Preparing to unpack .../libmnl0_1.0.3-5_amd64.deb ...
Unpacking libmnl0:amd64 (1.0.3-5) ...
Selecting previously unselected package libpopt0:amd64.
Preparing to unpack .../libpopt0_1.16-10_amd64.deb ...
Unpacking libpopt0:amd64 (1.16-10) ...
Selecting previously unselected package libssl1.0.0:amd64.
Preparing to unpack .../libssl1.0.0_1.0.2g-1ubuntu4.11_amd64.deb ...
Unpacking libssl1.0.0:amd64 (1.0.2g-1ubuntu4.11) ...
Selecting previously unselected package libpython3.5-minimal:amd64.
Preparing to unpack .../libpython3.5-minimal_3.5.2-2ubuntu0~16.04.4_amd64.deb ...
Unpacking libpython3.5-minimal:amd64 (3.5.2-2ubuntu0~16.04.4) ...
Selecting previously unselected package libexpat1:amd64.
Preparing to unpack .../libexpat1_2.1.0-7ubuntu0.16.04.3_amd64.deb ...
Unpacking libexpat1:amd64 (2.1.0-7ubuntu0.16.04.3) ...
Selecting previously unselected package python3.5-minimal.
Preparing to unpack .../python3.5-minimal_3.5.2-2ubuntu0~16.04.4_amd64.deb ...
Unpacking python3.5-minimal (3.5.2-2ubuntu0~16.04.4) ...
Selecting previously unselected package python3-minimal.
Preparing to unpack .../python3-minimal_3.5.1-3_amd64.deb ...
Unpacking python3-minimal (3.5.1-3) ...
Selecting previously unselected package mime-support.
Preparing to unpack .../mime-support_3.59ubuntu1_all.deb ...
Unpacking mime-support (3.59ubuntu1) ...
Selecting previously unselected package libmpdec2:amd64.
Preparing to unpack .../libmpdec2_2.4.2-1_amd64.deb ...
Unpacking libmpdec2:amd64 (2.4.2-1) ...
Selecting previously unselected package libsqlite3-0:amd64.
Preparing to unpack .../libsqlite3-0_3.11.0-1ubuntu1_amd64.deb ...
Unpacking libsqlite3-0:amd64 (3.11.0-1ubuntu1) ...
Selecting previously unselected package libpython3.5-stdlib:amd64.
Preparing to unpack .../libpython3.5-stdlib_3.5.2-2ubuntu0~16.04.4_amd64.deb ...
Unpacking libpython3.5-stdlib:amd64 (3.5.2-2ubuntu0~16.04.4) ...
Selecting previously unselected package python3.5.
Preparing to unpack .../python3.5_3.5.2-2ubuntu0~16.04.4_amd64.deb ...
Unpacking python3.5 (3.5.2-2ubuntu0~16.04.4) ...
Selecting previously unselected package libpython3-stdlib:amd64.
Preparing to unpack .../libpython3-stdlib_3.5.1-3_amd64.deb ...
Unpacking libpython3-stdlib:amd64 (3.5.1-3) ...
Selecting previously unselected package dh-python.
Preparing to unpack .../dh-python_2.20151103ubuntu1.1_all.deb ...
Unpacking dh-python (2.20151103ubuntu1.1) ...
Processing triggers for systemd (229-4ubuntu21.1) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Setting up libssl1.0.0:amd64 (1.0.2g-1ubuntu4.11) ...
debconf: unable to initialize frontend: Dialog
debconf: (TERM is not set, so the dialog frontend is not usable.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.22.1 /usr/local/share/perl/5.22.1 /usr/lib/x86_64-linux-gnu/perl5/5.22 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.22 /usr/share/perl/5.22 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base .) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype
Setting up libpython3.5-minimal:amd64 (3.5.2-2ubuntu0~16.04.4) ...
Setting up libexpat1:amd64 (2.1.0-7ubuntu0.16.04.3) ...
Setting up python3.5-minimal (3.5.2-2ubuntu0~16.04.4) ...
Setting up python3-minimal (3.5.1-3) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Selecting previously unselected package python3.
(Reading database ... 5805 files and directories currently installed.)
Preparing to unpack .../python3_3.5.1-3_amd64.deb ...
Unpacking python3 (3.5.1-3) ...
Selecting previously unselected package libgdbm3:amd64.
Preparing to unpack .../libgdbm3_1.8.3-13.1_amd64.deb ...
Unpacking libgdbm3:amd64 (1.8.3-13.1) ...
Selecting previously unselected package libxau6:amd64.
Preparing to unpack .../libxau6_1%3a1.0.8-1_amd64.deb ...
Unpacking libxau6:amd64 (1:1.0.8-1) ...
Selecting previously unselected package libxdmcp6:amd64.
Preparing to unpack .../libxdmcp6_1%3a1.1.2-1.1_amd64.deb ...
Unpacking libxdmcp6:amd64 (1:1.1.2-1.1) ...
Selecting previously unselected package libxcb1:amd64.
Preparing to unpack .../libxcb1_1.11.1-1ubuntu1_amd64.deb ...
Unpacking libxcb1:amd64 (1.11.1-1ubuntu1) ...
Selecting previously unselected package libx11-data.
Preparing to unpack .../libx11-data_2%3a1.6.3-1ubuntu2_all.deb ...
Unpacking libx11-data (2:1.6.3-1ubuntu2) ...
Selecting previously unselected package libx11-6:amd64.
Preparing to unpack .../libx11-6_2%3a1.6.3-1ubuntu2_amd64.deb ...
Unpacking libx11-6:amd64 (2:1.6.3-1ubuntu2) ...
Selecting previously unselected package libxext6:amd64.
Preparing to unpack .../libxext6_2%3a1.3.3-1_amd64.deb ...
Unpacking libxext6:amd64 (2:1.3.3-1) ...
Selecting previously unselected package sgml-base.
Preparing to unpack .../sgml-base_1.26+nmu4ubuntu1_all.deb ...
Unpacking sgml-base (1.26+nmu4ubuntu1) ...
Selecting previously unselected package fonts-dejavu-core.
Preparing to unpack .../fonts-dejavu-core_2.35-1_all.deb ...
Unpacking fonts-dejavu-core (2.35-1) ...
Selecting previously unselected package ucf.
Preparing to unpack .../archives/ucf_3.0036_all.deb ...
Moving old data out of the way
Unpacking ucf (3.0036) ...
Selecting previously unselected package fontconfig-config.
Preparing to unpack .../fontconfig-config_2.11.94-0ubuntu1.1_all.deb ...
Unpacking fontconfig-config (2.11.94-0ubuntu1.1) ...
Selecting previously unselected package libpng12-0:amd64.
Preparing to unpack .../libpng12-0_1.2.54-1ubuntu1_amd64.deb ...
Unpacking libpng12-0:amd64 (1.2.54-1ubuntu1) ...
Selecting previously unselected package libfreetype6:amd64.
Preparing to unpack .../libfreetype6_2.6.1-0.1ubuntu2.3_amd64.deb ...
Unpacking libfreetype6:amd64 (2.6.1-0.1ubuntu2.3) ...
Selecting previously unselected package libfontconfig1:amd64.
Preparing to unpack .../libfontconfig1_2.11.94-0ubuntu1.1_amd64.deb ...
Unpacking libfontconfig1:amd64 (2.11.94-0ubuntu1.1) ...
Selecting previously unselected package fontconfig.
Preparing to unpack .../fontconfig_2.11.94-0ubuntu1.1_amd64.deb ...
Unpacking fontconfig (2.11.94-0ubuntu1.1) ...
Selecting previously unselected package libasyncns0:amd64.
Preparing to unpack .../libasyncns0_0.8-5build1_amd64.deb ...
Unpacking libasyncns0:amd64 (0.8-5build1) ...
Selecting previously unselected package x11-common.
Preparing to unpack .../x11-common_1%3a7.7+13ubuntu3_all.deb ...
Unpacking x11-common (1:7.7+13ubuntu3) ...
Selecting previously unselected package libice6:amd64.
Preparing to unpack .../libice6_2%3a1.0.9-1_amd64.deb ...
Unpacking libice6:amd64 (2:1.0.9-1) ...
Selecting previously unselected package libjpeg-turbo8:amd64.
Preparing to unpack .../libjpeg-turbo8_1.4.2-0ubuntu3_amd64.deb ...
Unpacking libjpeg-turbo8:amd64 (1.4.2-0ubuntu3) ...
Selecting previously unselected package liblcms2-2:amd64.
Preparing to unpack .../liblcms2-2_2.6-3ubuntu2_amd64.deb ...
Unpacking liblcms2-2:amd64 (2.6-3ubuntu2) ...
Selecting previously unselected package libogg0:amd64.
Preparing to unpack .../libogg0_1.3.2-1_amd64.deb ...
Unpacking libogg0:amd64 (1.3.2-1) ...
Selecting previously unselected package libsm6:amd64.
Preparing to unpack .../libsm6_2%3a1.2.2-1_amd64.deb ...
Unpacking libsm6:amd64 (2:1.2.2-1) ...
Selecting previously unselected package libwrap0:amd64.
Preparing to unpack .../libwrap0_7.6.q-25_amd64.deb ...
Unpacking libwrap0:amd64 (7.6.q-25) ...
Selecting previously unselected package libxcomposite1:amd64.
Preparing to unpack .../libxcomposite1_1%3a0.4.4-1_amd64.deb ...
Unpacking libxcomposite1:amd64 (1:0.4.4-1) ...
Selecting previously unselected package libxdamage1:amd64.
Preparing to unpack .../libxdamage1_1%3a1.1.4-2_amd64.deb ...
Unpacking libxdamage1:amd64 (1:1.1.4-2) ...
Selecting previously unselected package libxfixes3:amd64.
Preparing to unpack .../libxfixes3_1%3a5.0.1-2_amd64.deb ...
Unpacking libxfixes3:amd64 (1:5.0.1-2) ...
Selecting previously unselected package libxinerama1:amd64.
Preparing to unpack .../libxinerama1_2%3a1.1.3-1_amd64.deb ...
Unpacking libxinerama1:amd64 (2:1.1.3-1) ...
Selecting previously unselected package libxshmfence1:amd64.
Preparing to unpack .../libxshmfence1_1.2-1_amd64.deb ...
Unpacking libxshmfence1:amd64 (1.2-1) ...
Selecting previously unselected package libxtst6:amd64.
Preparing to unpack .../libxtst6_2%3a1.2.2-1_amd64.deb ...
Unpacking libxtst6:amd64 (2:1.2.2-1) ...
Selecting previously unselected package libxxf86vm1:amd64.
Preparing to unpack .../libxxf86vm1_1%3a1.1.4-1_amd64.deb ...
Unpacking libxxf86vm1:amd64 (1:1.1.4-1) ...
Selecting previously unselected package perl-modules-5.22.
Preparing to unpack .../perl-modules-5.22_5.22.1-9ubuntu0.2_all.deb ...
Unpacking perl-modules-5.22 (5.22.1-9ubuntu0.2) ...
Selecting previously unselected package libperl5.22:amd64.
Preparing to unpack .../libperl5.22_5.22.1-9ubuntu0.2_amd64.deb ...
Unpacking libperl5.22:amd64 (5.22.1-9ubuntu0.2) ...
Selecting previously unselected package perl.
Preparing to unpack .../perl_5.22.1-9ubuntu0.2_amd64.deb ...
Unpacking perl (5.22.1-9ubuntu0.2) ...
Selecting previously unselected package libpython2.7-minimal:amd64.
Preparing to unpack .../libpython2.7-minimal_2.7.12-1ubuntu0~16.04.3_amd64.deb ...
Unpacking libpython2.7-minimal:amd64 (2.7.12-1ubuntu0~16.04.3) ...
Selecting previously unselected package python2.7-minimal.
Preparing to unpack .../python2.7-minimal_2.7.12-1ubuntu0~16.04.3_amd64.deb ...
Unpacking python2.7-minimal (2.7.12-1ubuntu0~16.04.3) ...
Selecting previously unselected package python-minimal.
Preparing to unpack .../python-minimal_2.7.12-1~16.04_amd64.deb ...
Unpacking python-minimal (2.7.12-1~16.04) ...
Selecting previously unselected package libffi6:amd64.
Preparing to unpack .../libffi6_3.2.1-4_amd64.deb ...
Unpacking libffi6:amd64 (3.2.1-4) ...
Selecting previously unselected package libpython2.7-stdlib:amd64.
Preparing to unpack .../libpython2.7-stdlib_2.7.12-1ubuntu0~16.04.3_amd64.deb ...
Unpacking libpython2.7-stdlib:amd64 (2.7.12-1ubuntu0~16.04.3) ...
Selecting previously unselected package python2.7.
Preparing to unpack .../python2.7_2.7.12-1ubuntu0~16.04.3_amd64.deb ...
Unpacking python2.7 (2.7.12-1ubuntu0~16.04.3) ...
Selecting previously unselected package libpython-stdlib:amd64.
Preparing to unpack .../libpython-stdlib_2.7.12-1~16.04_amd64.deb ...
Unpacking libpython-stdlib:amd64 (2.7.12-1~16.04) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Processing triggers for systemd (229-4ubuntu21.1) ...
Setting up libpython2.7-minimal:amd64 (2.7.12-1ubuntu0~16.04.3) ...
Setting up python2.7-minimal (2.7.12-1ubuntu0~16.04.3) ...
Linking and byte-compiling packages for runtime python2.7...
Setting up python-minimal (2.7.12-1~16.04) ...
Selecting previously unselected package python.
(Reading database ... 8955 files and directories currently installed.)
Preparing to unpack .../python_2.7.12-1~16.04_amd64.deb ...
Unpacking python (2.7.12-1~16.04) ...
Selecting previously unselected package libjbig0:amd64.
Preparing to unpack .../libjbig0_2.1-3.1_amd64.deb ...
Unpacking libjbig0:amd64 (2.1-3.1) ...
Selecting previously unselected package libgmp10:amd64.
Preparing to unpack .../libgmp10_2%3a6.1.0+dfsg-2_amd64.deb ...
Unpacking libgmp10:amd64 (2:6.1.0+dfsg-2) ...
Selecting previously unselected package libmpfr4:amd64.
Preparing to unpack .../libmpfr4_3.1.4-1_amd64.deb ...
Unpacking libmpfr4:amd64 (3.1.4-1) ...
Selecting previously unselected package libmpc3:amd64.
Preparing to unpack .../libmpc3_1.0.3-1_amd64.deb ...
Unpacking libmpc3:amd64 (1.0.3-1) ...
Selecting previously unselected package libtxc-dxtn-s2tc0:amd64.
Preparing to unpack .../libtxc-dxtn-s2tc0_0~git20131104-1.1_amd64.deb ...
Unpacking libtxc-dxtn-s2tc0:amd64 (0~git20131104-1.1) ...
Selecting previously unselected package libapt-inst2.0:amd64.
Preparing to unpack .../libapt-inst2.0_1.2.26_amd64.deb ...
Unpacking libapt-inst2.0:amd64 (1.2.26) ...
Selecting previously unselected package apt-utils.
Preparing to unpack .../apt-utils_1.2.26_amd64.deb ...
Unpacking apt-utils (1.2.26) ...
Selecting previously unselected package bzip2.
Preparing to unpack .../bzip2_1.0.6-8_amd64.deb ...
Unpacking bzip2 (1.0.6-8) ...
Selecting previously unselected package distro-info-data.
Preparing to unpack .../distro-info-data_0.28ubuntu0.7_all.deb ...


Adding debian:DST_ACES_CA_X6.pem
Adding debian:DST_Root_CA_X3.pem
Adding debian:Deutsche_Telekom_Root_CA_2.pem
Adding debian:DigiCert_Assured_ID_Root_CA.pem
Adding debian:DigiCert_Assured_ID_Root_G2.pem
Adding debian:DigiCert_Assured_ID_Root_G3.pem
Adding debian:DigiCert_Global_Root_CA.pem
Adding debian:DigiCert_Global_Root_G2.pem
Adding debian:DigiCert_Global_Root_G3.pem
Adding debian:DigiCert_High_Assurance_EV_Root_CA.pem
Adding debian:DigiCert_Trusted_Root_G4.pem
Adding debian:E-Tugra_Certification_Authority.pem
Adding debian:EC-ACC.pem
Adding debian:EE_Certification_Centre_Root_CA.pem
Adding debian:Entrust.net_Premium_2048_Secure_Server_CA.pem
Adding debian:Entrust_Root_Certification_Authority.pem
Adding debian:Entrust_Root_Certification_Authority_-_EC1.pem
Adding debian:Entrust_Root_Certification_Authority_-_G2.pem
Adding debian:GeoTrust_Global_CA.pem
Adding debian:GeoTrust_Global_CA_2.pem
Adding debian:GeoTrust_Primary_Certification_Authority.pem
Adding debian:GeoTrust_Primary_Certification_Authority_-_G2.pem
Adding debian:GeoTrust_Primary_Certification_Authority_-_G3.pem
Adding debian:GeoTrust_Universal_CA.pem
Adding debian:GeoTrust_Universal_CA_2.pem
Adding debian:GlobalSign_ECC_Root_CA_-_R4.pem
Adding debian:GlobalSign_ECC_Root_CA_-_R5.pem
Adding debian:GlobalSign_Root_CA.pem
Adding debian:GlobalSign_Root_CA_-_R2.pem
Adding debian:GlobalSign_Root_CA_-_R3.pem
Adding debian:Global_Chambersign_Root_-_2008.pem
Adding debian:Go_Daddy_Class_2_CA.pem
Adding debian:Go_Daddy_Root_Certificate_Authority_-_G2.pem
Adding debian:Hellenic_Academic_and_Research_Institutions_ECC_RootCA_2015.pem
Adding debian:Hellenic_Academic_and_Research_Institutions_RootCA_2011.pem
Adding debian:Hellenic_Academic_and_Research_Institutions_RootCA_2015.pem
Adding debian:Hongkong_Post_Root_CA_1.pem
Adding debian:ISRG_Root_X1.pem
Adding debian:IdenTrust_Commercial_Root_CA_1.pem
Adding debian:IdenTrust_Public_Sector_Root_CA_1.pem
Adding debian:Izenpe.com.pem
Adding debian:LuxTrust_Global_Root_2.pem
Adding debian:Microsec_e-Szigno_Root_CA_2009.pem
Adding debian:NetLock_Arany_=Class_Gold=_Főtanúsítvány.pem
Adding debian:Network_Solutions_Certificate_Authority.pem
Adding debian:OISTE_WISeKey_Global_Root_GA_CA.pem
Adding debian:OISTE_WISeKey_Global_Root_GB_CA.pem
Adding debian:OpenTrust_Root_CA_G1.pem
Adding debian:OpenTrust_Root_CA_G2.pem
Adding debian:OpenTrust_Root_CA_G3.pem
Adding debian:PSCProcert.pem
Adding debian:QuoVadis_Root_CA.pem
Adding debian:QuoVadis_Root_CA_1_G3.pem
Adding debian:QuoVadis_Root_CA_2.pem
Adding debian:QuoVadis_Root_CA_2_G3.pem
Adding debian:QuoVadis_Root_CA_3.pem
Adding debian:QuoVadis_Root_CA_3_G3.pem
Adding debian:SZAFIR_ROOT_CA2.pem
Adding debian:SecureSign_RootCA11.pem
Adding debian:SecureTrust_CA.pem
Adding debian:Secure_Global_CA.pem
Adding debian:Security_Communication_EV_RootCA1.pem
Adding debian:Security_Communication_RootCA2.pem
Adding debian:Security_Communication_Root_CA.pem
Adding debian:Sonera_Class_2_Root_CA.pem
Adding debian:Staat_der_Nederlanden_EV_Root_CA.pem
Adding debian:Staat_der_Nederlanden_Root_CA_-_G2.pem
Adding debian:Staat_der_Nederlanden_Root_CA_-_G3.pem
Adding debian:Starfield_Class_2_CA.pem
Adding debian:Starfield_Root_Certificate_Authority_-_G2.pem
Adding debian:Starfield_Services_Root_Certificate_Authority_-_G2.pem
Adding debian:SwissSign_Gold_CA_-_G2.pem
Adding debian:SwissSign_Silver_CA_-_G2.pem
Adding debian:Swisscom_Root_CA_1.pem
Adding debian:Swisscom_Root_CA_2.pem
Adding debian:Swisscom_Root_EV_CA_2.pem
Adding debian:T-TeleSec_GlobalRoot_Class_2.pem
Adding debian:T-TeleSec_GlobalRoot_Class_3.pem
Adding debian:TUBITAK_Kamu_SM_SSL_Kok_Sertifikasi_-_Surum_1.pem
Adding debian:TURKTRUST_Certificate_Services_Provider_Root_2007.pem
Adding debian:TWCA_Global_Root_CA.pem
Adding debian:TWCA_Root_Certification_Authority.pem
Adding debian:Taiwan_GRCA.pem
Adding debian:TeliaSonera_Root_CA_v1.pem
Adding debian:Trustis_FPS_Root_CA.pem
Adding debian:TÜBİTAK_UEKAE_Kök_Sertifika_Hizmet_Sağlayıcısı_-_Sürüm_3.pem
Adding debian:TÜRKTRUST_Elektronik_Sertifika_Hizmet_Sağlayıcısı_H5.pem
Adding debian:USERTrust_ECC_Certification_Authority.pem
Adding debian:USERTrust_RSA_Certification_Authority.pem
Adding debian:UTN_USERFirst_Hardware_Root_CA.pem
Adding debian:VeriSign_Class_3_Public_Primary_Certification_Authority_-_G4.pem
Adding debian:VeriSign_Class_3_Public_Primary_Certification_Authority_-_G5.pem
Adding debian:VeriSign_Universal_Root_Certification_Authority.pem
Adding debian:Verisign_Class_3_Public_Primary_Certification_Authority_-_G3.pem
Adding debian:Visa_eCommerce_Root.pem
Adding debian:XRamp_Global_CA_Root.pem
Adding debian:certSIGN_ROOT_CA.pem
Adding debian:ePKI_Root_Certification_Authority.pem
Adding debian:thawte_Primary_Root_CA.pem
Adding debian:thawte_Primary_Root_CA_-_G2.pem
Adding debian:thawte_Primary_Root_CA_-_G3.pem
done.
done.
Processing triggers for sgml-base (1.26+nmu4ubuntu1) ...
Processing triggers for dbus (1.10.6-1ubuntu3.3) ...
Removing intermediate container 87cc0b66220d
 ---> 5ec8a8cf43fb
Step 4/9 : RUN pip install mock grpcio
 ---> Running in 044551d33a13
Collecting mock
  Downloading mock-2.0.0-py2.py3-none-any.whl (56kB)
Collecting grpcio
  Downloading grpcio-1.10.0-cp27-cp27mu-manylinux1_x86_64.whl (7.4MB)
Collecting pbr>=0.11 (from mock)
  Downloading pbr-4.0.1-py2.py3-none-any.whl (97kB)
Collecting funcsigs>=1; python_version < "3.3" (from mock)
  Downloading funcsigs-1.0.2-py2.py3-none-any.whl
Collecting six>=1.9 (from mock)
  Downloading six-1.11.0-py2.py3-none-any.whl
Collecting enum34>=1.0.4 (from grpcio)
  Downloading enum34-1.1.6-py2-none-any.whl
Collecting protobuf>=3.5.0.post1 (from grpcio)
  Downloading protobuf-3.5.2.post1-cp27-cp27mu-manylinux1_x86_64.whl (6.4MB)
Collecting futures>=2.2.0 (from grpcio)
  Downloading futures-3.2.0-py2-none-any.whl
Requirement already satisfied (use --upgrade to upgrade): setuptools in /usr/lib/python2.7/dist-packages (from protobuf>=3.5.0.post1->grpcio)
Installing collected packages: pbr, funcsigs, six, mock, enum34, protobuf, futures, grpcio
Successfully installed enum34-1.1.6 funcsigs-1.0.2 futures-3.2.0 grpcio-1.10.0 mock-2.0.0 pbr-4.0.1 protobuf-3.5.2.post1 six-1.11.0
You are using pip version 8.1.1, however version 9.0.3 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
Removing intermediate container 044551d33a13
 ---> 8bbd54c3a0dc
Step 5/9 : ENV BAZELRC /root/.bazelrc
 ---> Running in f84ccd5212e9
Removing intermediate container f84ccd5212e9
 ---> 663d5c2fa4cd
Step 6/9 : ENV BAZEL_VERSION 0.5.4
 ---> Running in ba4b4c3b9fa5
Removing intermediate container ba4b4c3b9fa5
 ---> 1582636efa2f
Step 7/9 : WORKDIR /
Removing intermediate container 3e727dba28b8
 ---> dcc08dbc3510
Step 8/9 : RUN mkdir /bazel &&     cd /bazel &&     curl -fSsL -O https://github.com/bazelbuild/bazel/releases/download/$BAZEL_VERSION/bazel-$BAZEL_VERSION-installer-linux-x86_64.sh &&     curl -fSsL -o /bazel/LICENSE.txt https://raw.githubusercontent.com/bazelbuild/bazel/master/LICENSE &&     chmod +x bazel-*.sh &&     ./bazel-$BAZEL_VERSION-installer-linux-x86_64.sh &&     cd / &&     rm -f /bazel/bazel-$BAZEL_VERSION-installer-linux-x86_64.sh
 ---> Running in 0818bf45353b
Bazel installer
---------------

Bazel is bundled with software licensed under the GPLv2 with Classpath exception.
You can find the sources next to the installer on our release page:
   https://github.com/bazelbuild/bazel/releases

# Release 0.5.4 (2017-08-25)

Baseline: 6563b2d42d29196432d5fcafa0144b8371fbb028

Cherry picks:
   + d4fa181f8607c35230b7efa1ce94188b51508962:
     Use getExecPathString when getting bash_main_file
   + 837e1b3d4859140d29aaa6bbab8fbb008e6d701e:
     Windows, sh_bin. launcher: export runfiles envvars
   + fe9ba893c0ebec19228086356af5fa8d81f2809b:
     grpc: Consolidate gRPC code from BES and Remote Execution. Fixes
     #3460, #3486
   + e8d4366cd374fba92f1425de0d475411c8defda4:
     Automated rollback of commit
     496d3ded0bce12b7371a93e1183ba30e6aa88032.
   + 242a43449dd44a22857f6ce95f7cc6a7e134d298:
     bes,remote: update default auth scope.
   + 793b409eeae2b42be7fed58251afa87b5733ca4d:
     Windows, sh_bin. launcher: fix manifest path
   + 7e4fbbe4ab3915a57b2187408c3909e5cd6c6013:
     Add --windows_exe_launcher option
   + 91fb38e92ace6cf14ce5da6527d71320b4e3f3d2:
     remote_worker: Serialize fork() calls. Fixes #3356
   + b79a9fcd40f448d3aebb2b93a2ebe80d09b38408:
     Quote python_path and launcher in
     python_stub_template_windows.txt
   + 4a2e17f85fc8450aa084b201c5f24b30010c5987:
     Add build_windows_jni.sh back
   + ce61d638197251f71ed90db74843b55d9c2e9ae5:
     don't use methods and classes removed in upstream dx RELNOTES:
     update dexing tools to Android SDK 26.0.1
   + 5393a4996d701fa192964a35cbb75e558a0599c0:
     Make Bazel enforce requirement on build-tools 26.0.1 or later.
   + 5fac03570f80856c063c6019f5beb3bdc1672dee:
     Fix --verbose_failures w/ sandboxing to print the full command
     line
   + f7bd1acf1f96bb7e3e19edb9483d9e07eb5af070:
     Only patch in C++ compile features when they are not already
     defined in crosstool
   + d7f5c120417bc2d2344dfb285322355f225d9153:
     Bump python-gflags to 3.1.0, take two
   + 3cb136d5451e9d8af58f9a99990cad0592df101a:
     Add python to bazel's dockerfiles

New features:

  - Do not disable fully dynamic linking with ThinLTO when invoked
    via LIPO options.

Important changes:

  - Ignore --glibc in the Android transition.
  - Remove --experimental_android_use_singlejar_for_multidex.
  - nocopts now also filter copts
  - The Build Event Service (BES) client now properly supports
    Google Applicaton Default Credentials.
  - update dexing tools to Android SDK 26.0.1
  - Bazel Android support now requires build-tools 26.0.1 or later.
  - Fix a bug in the remote_worker that would at times make it crash on Linux. See #3356
  - The java_proto_library rule now supports generated sources. See #2265

## Build informations
   - [Commit](https://github.com/bazelbuild/bazel/commit/67f23f5)
Uncompressing.......

Bazel is now installed!

Make sure you have "/usr/local/bin" in your path. You can also activate bash
completion by adding the following line to your ~/.bashrc:
  source /usr/local/lib/bazel/bin/bazel-complete.bash

See http://bazel.build/docs/getting-started.html to start a new project!
Removing intermediate container 0818bf45353b
 ---> b5e48bea04ae
Step 9/9 : CMD ["/bin/bash"]
 ---> Running in eec8219b5bef
Removing intermediate container eec8219b5bef
 ---> 69e7c3fa252a
Successfully built 69e7c3fa252a
Successfully tagged dhankar/tensorflow-serving-devel:latest
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ls
Dockerfile.devel
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a[sudo] password for dhankar: 
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS                         PORTS               NAMES
c2124e6f3fc5        tensorflow/tensorflow             "/run_jupyter.sh --a…"   About an hour ago   Exited (0) About an hour ago                       serene_chandrasekhar
2c406ec20315        ddrohit/new_image_ubuntu_qgis_3   "bash"                   13 days ago         Exited (127) 13 days ago                           cranky_heisenberg
51222fc2ea78        ddrohit/new_image_ubuntu_qgis_2   "bash"                   13 days ago         Exited (0) 13 days ago                             elastic_colden
1ac88cc06e5f        ddrohit/new_image_ubuntu_qgis_2   "bash"                   13 days ago         Exited (139) 13 days ago                           goofy_hopper
3501e1023cf0        ddrohit/new_image_ubuntu_qgis_2   "bash"                   13 days ago         Exited (2) 13 days ago                             naughty_murdock
6d3c3634ca4f        ddrohit/new_image_ubuntu_qgis_1   "bash"                   2 weeks ago         Exited (1) 2 weeks ago                             eloquent_engelbart1
5c2ed1274cc4        ddrohit/new_image_ubuntu_qgis_1   "bash"                   2 weeks ago         Exited (127) 2 weeks ago                           confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis     "bash"                   2 weeks ago         Exited (0) 2 weeks ago                             agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis     "bash"                   2 weeks ago         Exited (1) 2 weeks ago                             agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1        "bash"                   2 weeks ago         Exited (127) 2 weeks ago                           stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu          "bash"                   2 weeks ago         Exited (127) 2 weeks ago                           sleepy_northcutt
82d279189cbf        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                             kind_hugle
8c124734e956        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                             zen_einstein
0976a20a1d0f        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                             suspicious_jones
e1aa2dbeb05b        ubuntu                            "bash"                   2 weeks ago         Exited (127) 2 weeks ago                           jolly_swirles
be5b8099d8fd        ubuntu                            "bash"                   2 weeks ago         Exited (0) 2 weeks ago                             practical_fermat
c995d7c5e17e        ubuntu                            "bash"                   2 weeks ago         Exited (130) 2 weeks ago                           jovial_kirch
91761424a8d7        hello-world                       "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                             focused_chatterjee
74bc5baaad36        kartoza/qgis-desktop              "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                             gifted_knuth
5adb571f280a        kartoza/qgis-desktop              "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                             nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker run -it $USER/tensorflow-serving-devel
docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.35/containers/create: dial unix /var/run/docker.sock: connect: permission denied.
See 'docker run --help'.
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker run -it $USER/tensorflow-serving-develroot@44ada9c5e1d3:/# 
root@44ada9c5e1d3:/# # WE ARE IN :) 
root@44ada9c5e1d3:/# 
root@44ada9c5e1d3:/# dir
bazel  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run	sbin  srv  sys	tmp  usr  var
root@44ada9c5e1d3:/# 
root@44ada9c5e1d3:/# git clone --recurse-submodules https://github.com/tensorflow/serving
Cloning into 'serving'...
remote: Counting objects: 6268, done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 6268 (delta 11), reused 14 (delta 5), pack-reused 6241
Receiving objects: 100% (6268/6268), 2.38 MiB | 1.05 MiB/s, done.
Resolving deltas: 100% (4468/4468), done.
Checking connectivity... done.
root@44ada9c5e1d3:/# cd serving/tensorflow
bash: cd: serving/tensorflow: No such file or directory
root@44ada9c5e1d3:/# ./configure
bash: ./configure: No such file or directory
root@44ada9c5e1d3:/# cd ..
root@44ada9c5e1d3:/# bazel test tensorflow_serving/...
Extracting Bazel installation...
ERROR: The 'test' command is only supported from within a workspace.
root@44ada9c5e1d3:/# git clone --recurse-submodules https://github.com/tensorflow/serving
fatal: destination path 'serving' already exists and is not an empty directory.
root@44ada9c5e1d3:/# dir
bazel  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run	sbin  serving  srv  sys  tmp  usr  var
root@44ada9c5e1d3:/# cd serving
root@44ada9c5e1d3:/serving# dir
AUTHORS  CONTRIBUTING.md  LICENSE  README.md  RELEASE.md  WORKSPACE  tensorflow_serving  tools
root@44ada9c5e1d3:/serving# 
root@44ada9c5e1d3:/serving# cd tensorflow_serving
root@44ada9c5e1d3:/serving/tensorflow_serving# dir
BUILD  batching  core	  g3doc		 repo.bzl   servables	 sources    tools  workspace.bzl
apis   config	 example  model_servers  resources  serving.bzl  test_util  util
root@44ada9c5e1d3:/serving/tensorflow_serving# 
root@44ada9c5e1d3:/serving/tensorflow_serving# ./config
bash: ./config: Is a directory
root@44ada9c5e1d3:/serving/tensorflow_serving# cd config
root@44ada9c5e1d3:/serving/tensorflow_serving/config# dir
BUILD  log_collector_config.proto  logging_config.proto  model_server_config.proto  platform_config.proto
root@44ada9c5e1d3:/serving/tensorflow_serving/config# 
root@44ada9c5e1d3:/serving/tensorflow_serving/config# cd ..
root@44ada9c5e1d3:/serving/tensorflow_serving# bazel build -c opt tensorflow_serving/...
...........................
ERROR: no targets found beneath 'tensorflow_serving/tensorflow_serving'.
INFO: Elapsed time: 0.860s
root@44ada9c5e1d3:/serving/tensorflow_serving# cd ..
root@44ada9c5e1d3:/serving# bazel build -c opt tensorflow_serving/...
WARNING: /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/protobuf_archive/WORKSPACE:1: Workspace name in /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/protobuf_archive/WORKSPACE (@com_google_protobuf) does not match the name given in the repository's definition (@protobuf_archive); this will cause a build error in future versions.
WARNING: /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/grpc/WORKSPACE:1: Workspace name in /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/grpc/WORKSPACE (@com_github_grpc_grpc) does not match the name given in the repository's definition (@grpc); this will cause a build error in future versions.
WARNING: /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/org_tensorflow/tensorflow/core/BUILD:1865:1: in includes attribute of cc_library rule @org_tensorflow//tensorflow/core:framework_headers_lib: '../../../../external/nsync/public' resolves to 'external/nsync/public' not below the relative path of its package 'external/org_tensorflow/tensorflow/core'. This will be an error in the future. Since this rule was created by the macro 'cc_header_only_library', the error might have been caused by the macro implementation in /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/org_tensorflow/tensorflow/tensorflow.bzl:1163:30.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:655:1: in cc_library rule //tensorflow_serving/servables/tensorflow:regressor: target '//tensorflow_serving/servables/tensorflow:regressor' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle_lite': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:655:1: in cc_library rule //tensorflow_serving/servables/tensorflow:regressor: target '//tensorflow_serving/servables/tensorflow:regressor' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:signature_lite': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:524:1: in cc_library rule //tensorflow_serving/servables/tensorflow:classifier: target '//tensorflow_serving/servables/tensorflow:classifier' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle_lite': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:524:1: in cc_library rule //tensorflow_serving/servables/tensorflow:classifier: target '//tensorflow_serving/servables/tensorflow:classifier' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:signature_lite': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:678:1: in cc_test rule //tensorflow_serving/servables/tensorflow:regressor_test: target '//tensorflow_serving/servables/tensorflow:regressor_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:547:1: in cc_test rule //tensorflow_serving/servables/tensorflow:classifier_test: target '//tensorflow_serving/servables/tensorflow:classifier_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/batching/BUILD:72:1: in cc_test rule //tensorflow_serving/batching:batching_session_test: target '//tensorflow_serving/batching:batching_session_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:121:1: in cc_library rule //tensorflow_serving/servables/tensorflow:session_bundle_factory: target '//tensorflow_serving/servables/tensorflow:session_bundle_factory' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:209:1: in cc_library rule //tensorflow_serving/servables/tensorflow:session_bundle_source_adapter: target '//tensorflow_serving/servables/tensorflow:session_bundle_source_adapter' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:61:1: in cc_test rule //tensorflow_serving/servables/tensorflow:bundle_factory_util_test: target '//tensorflow_serving/servables/tensorflow:bundle_factory_util_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:231:1: in cc_test rule //tensorflow_serving/servables/tensorflow:session_bundle_source_adapter_test: target '//tensorflow_serving/servables/tensorflow:session_bundle_source_adapter_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:142:1: in cc_test rule //tensorflow_serving/servables/tensorflow:session_bundle_factory_test: target '//tensorflow_serving/servables/tensorflow:session_bundle_factory_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:571:1: in cc_library rule //tensorflow_serving/servables/tensorflow:classification_service: target '//tensorflow_serving/servables/tensorflow:classification_service' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:571:1: in cc_library rule //tensorflow_serving/servables/tensorflow:classification_service: target '//tensorflow_serving/servables/tensorflow:classification_service' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:signature': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:613:1: in cc_library rule //tensorflow_serving/servables/tensorflow:regression_service: target '//tensorflow_serving/servables/tensorflow:regression_service' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:613:1: in cc_library rule //tensorflow_serving/servables/tensorflow:regression_service: target '//tensorflow_serving/servables/tensorflow:regression_service' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:signature': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:417:1: in cc_library rule //tensorflow_serving/servables/tensorflow:predict_impl: target '//tensorflow_serving/servables/tensorflow:predict_impl' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:417:1: in cc_library rule //tensorflow_serving/servables/tensorflow:predict_impl: target '//tensorflow_serving/servables/tensorflow:predict_impl' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:signature': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:701:1: in cc_library rule //tensorflow_serving/servables/tensorflow:multi_inference: target '//tensorflow_serving/servables/tensorflow:multi_inference' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:438:1: in cc_library rule //tensorflow_serving/servables/tensorflow:get_model_metadata_impl: target '//tensorflow_serving/servables/tensorflow:get_model_metadata_impl' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:456:1: in cc_test rule //tensorflow_serving/servables/tensorflow:get_model_metadata_impl_test: target '//tensorflow_serving/servables/tensorflow:get_model_metadata_impl_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/BUILD:492:1: in cc_test rule //tensorflow_serving/servables/tensorflow:predict_impl_test: target '//tensorflow_serving/servables/tensorflow:predict_impl_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/model_servers/BUILD:127:1: in cc_test rule //tensorflow_serving/model_servers:get_model_status_impl_test: target '//tensorflow_serving/model_servers:get_model_status_impl_test' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:session_bundle': No longer supported. Switch to SavedModel immediately.
WARNING: /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/org_tensorflow/tensorflow/contrib/learn/BUILD:15:1: in py_library rule @org_tensorflow//tensorflow/contrib/learn:learn: target '@org_tensorflow//tensorflow/contrib/learn:learn' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:exporter': No longer supported. Switch to SavedModel immediately.
WARNING: /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/org_tensorflow/tensorflow/contrib/learn/BUILD:15:1: in py_library rule @org_tensorflow//tensorflow/contrib/learn:learn: target '@org_tensorflow//tensorflow/contrib/learn:learn' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:gc': No longer supported. Switch to SavedModel immediately.
WARNING: /serving/tensorflow_serving/servables/tensorflow/testdata/BUILD:26:1: in py_binary rule //tensorflow_serving/servables/tensorflow/testdata:export_half_plus_two: target '//tensorflow_serving/servables/tensorflow/testdata:export_half_plus_two' depends on deprecated target '@org_tensorflow//tensorflow/contrib/session_bundle:exporter': No longer supported. Switch to SavedModel immediately.
ERROR: /serving/tensorflow_serving/example/BUILD:55:1: no such package '@inception_model//inception': Error downloading [https://mirror.bazel.build/github.com/tensorflow/models/archive/6fc65ee60ac39be0445e5a311b40dc7ccce214d0.tar.gz, https://github.com/tensorflow/models/archive/6fc65ee60ac39be0445e5a311b40dc7ccce214d0.tar.gz] to /root/.cache/bazel/_bazel_root/f8d1071c69ea316497c31e40fe01608c/external/inception_model/6fc65ee60ac39be0445e5a311b40dc7ccce214d0.tar.gz: Checksum was 69875545c490cdd59a39d58627a57edfef8dfebba99bd4e96cd8c6f980e11e34 but wanted 7a908017d60fca54c80405527576f08dbf8d130efe6a53791639ff3b26afffbc and referenced by '//tensorflow_serving/example:inception_saved_model'.
ERROR: Analysis of target '//tensorflow_serving/example:inception_saved_model' failed; build aborted.
INFO: Elapsed time: 131.235s
root@44ada9c5e1d3:/serving# 
root@44ada9c5e1d3:/serving# dir
AUTHORS  CONTRIBUTING.md  LICENSE  README.md  RELEASE.md  WORKSPACE  tensorflow_serving  tools
root@44ada9c5e1d3:/serving# 
root@44ada9c5e1d3:/serving# exit
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a[sudo] password for dhankar: 
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                      PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              41 minutes ago      Exited (0) 21 seconds ago                       upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   2 hours ago         Exited (0) 2 hours ago                          serene_chandrasekhar
2c406ec20315        ddrohit/new_image_ubuntu_qgis_3    "bash"                   13 days ago         Exited (127) 13 days ago                        cranky_heisenberg
51222fc2ea78        ddrohit/new_image_ubuntu_qgis_2    "bash"                   13 days ago         Exited (0) 13 days ago                          elastic_colden
1ac88cc06e5f        ddrohit/new_image_ubuntu_qgis_2    "bash"                   13 days ago         Exited (139) 13 days ago                        goofy_hopper
3501e1023cf0        ddrohit/new_image_ubuntu_qgis_2    "bash"                   13 days ago         Exited (2) 13 days ago                          naughty_murdock
6d3c3634ca4f        ddrohit/new_image_ubuntu_qgis_1    "bash"                   2 weeks ago         Exited (1) 2 weeks ago                          eloquent_engelbart1
5c2ed1274cc4        ddrohit/new_image_ubuntu_qgis_1    "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                          agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                        jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                          practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                        jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                          focused_chatterjee
74bc5baaad36        kartoza/qgis-desktop               "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                          gifted_knuth
5adb571f280a        kartoza/qgis-desktop               "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                          nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
[sudo] password for dhankar: 
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        10 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis_3    latest              1c8eb8183583        2 weeks ago         2.56GB
ddrohit/new_image_ubuntu_qgis_2    latest              28f9802044f2        2 weeks ago         2.11GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        4 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
kartoza/qgis-desktop               latest              c52dc19f7cb8        2 years ago         1.69GB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker rmi c52dc19f7cb8
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Delete http://%2Fvar%2Frun%2Fdocker.sock/v1.35/images/c52dc19f7cb8: dial unix /var/run/docker.sock: connect: permission denied
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi c52dc19f7cb8
Error response from daemon: conflict: unable to delete c52dc19f7cb8 (must be forced) - image is being used by stopped container 74bc5baaad36
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f c52dc19f7cb8
Untagged: kartoza/qgis-desktop:latest
Untagged: kartoza/qgis-desktop@sha256:2099ac982cf198cdff1b0ef6e1182ebb5b873ea1f0022461305b09d4e48ce2aa
Deleted: sha256:c52dc19f7cb80d7de0c2820348cd5a97c7866a41cedf6861946aa3bb819bdd90
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        10 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis_3    latest              1c8eb8183583        2 weeks ago         2.56GB
ddrohit/new_image_ubuntu_qgis_2    latest              28f9802044f2        2 weeks ago         2.11GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        4 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ## FART --- Docker - as seen above ---kartoza/qgis-desktop               latest              c52dc19f7cb8        2 years ago         1.69GB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ## Above image REMOVED after giving the FORCED - f FLAG - as the CONTAINER was Still Running 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -aCONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              10 hours ago        Exited (0) 9 hours ago                         upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   11 hours ago        Exited (0) 11 hours ago                        serene_chandrasekhar
2c406ec20315        ddrohit/new_image_ubuntu_qgis_3    "bash"                   13 days ago         Exited (127) 13 days ago                       cranky_heisenberg
51222fc2ea78        ddrohit/new_image_ubuntu_qgis_2    "bash"                   13 days ago         Exited (0) 13 days ago                         elastic_colden
1ac88cc06e5f        ddrohit/new_image_ubuntu_qgis_2    "bash"                   2 weeks ago         Exited (139) 2 weeks ago                       goofy_hopper
3501e1023cf0        ddrohit/new_image_ubuntu_qgis_2    "bash"                   2 weeks ago         Exited (2) 2 weeks ago                         naughty_murdock
6d3c3634ca4f        ddrohit/new_image_ubuntu_qgis_1    "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         eloquent_engelbart1
5c2ed1274cc4        ddrohit/new_image_ubuntu_qgis_1    "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker imagesREPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        10 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis_3    latest              1c8eb8183583        2 weeks ago         2.56GB
ddrohit/new_image_ubuntu_qgis_2    latest              28f9802044f2        2 weeks ago         2.11GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        4 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ## FART -- seen above - IMAGE NAME == hello-world is still running in CONTAINER ID ==91761424a8d7 ,  also with ALIAS NAME == focused_chatterjee 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 

``` python

#

_image_ubuntu_qgis_2    latest              28f9802044f2        2 weeks ago         2.11GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        4 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ## FART --- Docker - as seen above ---kartoza/qgis-desktop               latest              c52dc19f7cb8        2 years ago         1.69GB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ## Above image REMOVED after giving the FORCED - f FLAG - as the CONTAINER was Still Running 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -aCONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              10 hours ago        Exited (0) 9 hours ago                         upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   11 hours ago        Exited (0) 11 hours ago                        serene_chandrasekhar
2c406ec20315        ddrohit/new_image_ubuntu_qgis_3    "bash"                   13 days ago         Exited (127) 13 days ago                       cranky_heisenberg
51222fc2ea78        ddrohit/new_image_ubuntu_qgis_2    "bash"                   13 days ago         Exited (0) 13 days ago                         elastic_colden
1ac88cc06e5f        ddrohit/new_image_ubuntu_qgis_2    "bash"                   2 weeks ago         Exited (139) 2 weeks ago                       goofy_hopper
3501e1023cf0        ddrohit/new_image_ubuntu_qgis_2    "bash"                   2 weeks ago         Exited (2) 2 weeks ago                         naughty_murdock
6d3c3634ca4f        ddrohit/new_image_ubuntu_qgis_1    "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         eloquent_engelbart1
5c2ed1274cc4        ddrohit/new_image_ubuntu_qgis_1    "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker imagesREPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        10 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis_3    latest              1c8eb8183583        2 weeks ago         2.56GB
ddrohit/new_image_ubuntu_qgis_2    latest              28f9802044f2        2 weeks ago         2.11GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        4 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ## FART -- seen above - IMAGE NAME == hello-world is still running in CONTAINER ID ==91761424a8d7 ,  also with ALIAS NAME == focused_chatterjee 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f dd7ddf7eb0f1
[sudo] password for dhankar: 
Error response from daemon: conflict: unable to delete dd7ddf7eb0f1 (cannot be forced) - image has dependent child images
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ docker inspect --format='{{.Id}} {{.Parent}}' $(docker images --filter since=dd7ddf7eb0f1 -q)
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.35/images/json?filters=%7B%22since%22%3A%7B%22dd7ddf7eb0f1%22%3Atrue%7D%7D: dial unix /var/run/docker.sock: connect: permission denied
"docker inspect" requires at least 1 argument.
See 'docker inspect --help'.

Usage:  docker inspect [OPTIONS] NAME|ID [NAME|ID...] [flags]

Return low-level information on Docker objects
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker inspect --format='{{.Id}} {{.Parent}}' $(docker images --filter since=dd7ddf7eb0f1 -q)
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.35/images/json?filters=%7B%22since%22%3A%7B%22dd7ddf7eb0f1%22%3Atrue%7D%7D: dial unix /var/run/docker.sock: connect: permission denied
"docker inspect" requires at least 1 argument.
See 'docker inspect --help'.

Usage:  docker inspect [OPTIONS] NAME|ID [NAME|ID...] [flags]

Return low-level information on Docker objects
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f 1c8eb8183583
Untagged: ddrohit/new_image_ubuntu_qgis_3:latest
Deleted: sha256:1c8eb8183583f57a94431685e7feade42632939193c12107fa347f7048b128c8
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker imagesREPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis_2    latest              28f9802044f2        2 weeks ago         2.11GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        5 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f 28f9802044f2
Untagged: ddrohit/new_image_ubuntu_qgis_2:latest
Deleted: sha256:28f9802044f25a4a64571a7adcc2796b109790acd59c544dfcebe8005fe09a09
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis_1    latest              1049036b6e1a        2 weeks ago         1.92GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        5 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f 1049036b6e1a
[sudo] password for dhankar: 
Untagged: ddrohit/new_image_ubuntu_qgis_1:latest
Deleted: sha256:1049036b6e1a4d3c78e1070acc87bf01ef25dfa8043c234a8c6630fa9cdd2b18
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   15 hours ago        Exited (0) 15 hours ago                        serene_chandrasekhar
2c406ec20315        1c8eb8183583                       "bash"                   2 weeks ago         Exited (127) 13 days ago                       cranky_heisenberg
51222fc2ea78        28f9802044f2                       "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         elastic_colden
1ac88cc06e5f        28f9802044f2                       "bash"                   2 weeks ago         Exited (139) 2 weeks ago                       goofy_hopper
3501e1023cf0        28f9802044f2                       "bash"                   2 weeks ago         Exited (2) 2 weeks ago                         naughty_murdock
6d3c3634ca4f        1049036b6e1a                       "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         eloquent_engelbart1
5c2ed1274cc4        1049036b6e1a                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 51222fc2ea78
51222fc2ea78
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   15 hours ago        Exited (0) 15 hours ago                        serene_chandrasekhar
2c406ec20315        1c8eb8183583                       "bash"                   2 weeks ago         Exited (127) 13 days ago                       cranky_heisenberg
1ac88cc06e5f        28f9802044f2                       "bash"                   2 weeks ago         Exited (139) 2 weeks ago                       goofy_hopper
3501e1023cf0        28f9802044f2                       "bash"                   2 weeks ago         Exited (2) 2 weeks ago                         naughty_murdock
6d3c3634ca4f        1049036b6e1a                       "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         eloquent_engelbart1
5c2ed1274cc4        1049036b6e1a                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 51222fc2ea78
Error: No such container: 51222fc2ea78
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        5 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   15 hours ago        Exited (0) 15 hours ago                        serene_chandrasekhar
2c406ec20315        1c8eb8183583                       "bash"                   2 weeks ago         Exited (127) 13 days ago                       cranky_heisenberg
1ac88cc06e5f        28f9802044f2                       "bash"                   2 weeks ago         Exited (139) 2 weeks ago                       goofy_hopper
3501e1023cf0        28f9802044f2                       "bash"                   2 weeks ago         Exited (2) 2 weeks ago                         naughty_murdock
6d3c3634ca4f        1049036b6e1a                       "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         eloquent_engelbart1
5c2ed1274cc4        1049036b6e1a                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       confident_villani
9a76be0e57ea        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         agitated_pare
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 1ac88cc06e5f
1ac88cc06e5f
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 3501e1023cf0
3501e1023cf0
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 6d3c3634ca4f
6d3c3634ca4f
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 5c2ed1274cc4
5c2ed1274cc4
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 9a76be0e57ea
9a76be0e57ea
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
c2124e6f3fc5        tensorflow/tensorflow              "/run_jupyter.sh --a…"   15 hours ago        Exited (0) 15 hours ago                        serene_chandrasekhar
2c406ec20315        1c8eb8183583                       "bash"                   2 weeks ago         Exited (127) 13 days ago                       cranky_heisenberg
05b8dc1b5e9f        ddrohit/new_image_ubuntu_qgis      "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        ddrohit/new_image_ubuntu_1         "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        ddrohit/new_image_ubuntu           "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ddrohit/new_image_ubuntu_qgis      latest              725c626af4e0        2 weeks ago         1.62GB
ddrohit/new_image_ubuntu_1         latest              a01b86204c33        2 weeks ago         864MB
ddrohit/new_image_ubuntu           latest              dd7ddf7eb0f1        2 weeks ago         340MB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        5 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f 725c626af4e0
Untagged: ddrohit/new_image_ubuntu_qgis:latest
Deleted: sha256:725c626af4e0d03cc5e9a17e4e42247e3fa5be96fc98a56522a807aff2cbe373
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f a01b86204c33
Untagged: ddrohit/new_image_ubuntu_1:latest
Deleted: sha256:a01b86204c330614f4e97067fcccd5b3e33431d57f4a917a880bced629a6c294
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f dd7ddf7eb0f1
Untagged: ddrohit/new_image_ubuntu:latest
Deleted: sha256:dd7ddf7eb0f11244c1472fc9edbd5bce8124ac79b671ac91733268177f97b451
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f f975c5035748 
Error response from daemon: conflict: unable to delete f975c5035748 (cannot be forced) - image has dependent child images
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
tensorflow/tensorflow              latest              414b6e39764a        5 weeks ago         1.27GB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rmi -f 414b6e39764a
Untagged: tensorflow/tensorflow:latest
Untagged: tensorflow/tensorflow@sha256:1e1c7666928ebb8eb68e2f37422746eb345d7633dc4822bc21615c96868737eb
Deleted: sha256:414b6e39764a7d17d46cd9c26646febd97d7160112845de9a52992dffd12b485
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
c2124e6f3fc5        414b6e39764a                       "/run_jupyter.sh --a…"   15 hours ago        Exited (0) 15 hours ago                        serene_chandrasekhar
2c406ec20315        1c8eb8183583                       "bash"                   2 weeks ago         Exited (127) 13 days ago                       cranky_heisenberg
05b8dc1b5e9f        725c626af4e0                       "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        a01b86204c33                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        dd7ddf7eb0f1                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
8c124734e956        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         zen_einstein
0976a20a1d0f        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         suspicious_jones
e1aa2dbeb05b        ubuntu                             "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       jolly_swirles
be5b8099d8fd        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         practical_fermat
c995d7c5e17e        ubuntu                             "bash"                   2 weeks ago         Exited (130) 2 weeks ago                       jovial_kirch
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm c995d7c5e17e
c995d7c5e17e
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm be5b8099d8fd
be5b8099d8fd
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm e1aa2dbeb05b
e1aa2dbeb05b
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 0976a20a1d0f
0976a20a1d0f
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 8c124734e956
8c124734e956
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
c2124e6f3fc5        414b6e39764a                       "/run_jupyter.sh --a…"   15 hours ago        Exited (0) 15 hours ago                        serene_chandrasekhar
2c406ec20315        1c8eb8183583                       "bash"                   2 weeks ago         Exited (127) 13 days ago                       cranky_heisenberg
05b8dc1b5e9f        725c626af4e0                       "bash"                   2 weeks ago         Exited (1) 2 weeks ago                         agitated_swanson
fc107394f848        a01b86204c33                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        dd7ddf7eb0f1                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
dhankar/tensorflow-serving-devel   latest              69e7c3fa252a        14 hours ago        1.1GB
ubuntu                             16.04               f975c5035748        4 weeks ago         112MB
ubuntu                             latest              f975c5035748        4 weeks ago         112MB
hello-world                        latest              f2a91732366c        4 months ago        1.85kB
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm c2124e6f3fc5
c2124e6f3fc5
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 2c406ec20315
2c406ec20315
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker rm 05b8dc1b5e9f
05b8dc1b5e9f
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ sudo docker ps -a
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS                     PORTS               NAMES
44ada9c5e1d3        dhankar/tensorflow-serving-devel   "/bin/bash"              14 hours ago        Exited (0) 13 hours ago                        upbeat_mccarthy
fc107394f848        a01b86204c33                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       stupefied_meitner
8f5ea764d4b7        dd7ddf7eb0f1                       "bash"                   2 weeks ago         Exited (127) 2 weeks ago                       sleepy_northcutt
82d279189cbf        ubuntu                             "bash"                   2 weeks ago         Exited (0) 2 weeks ago                         kind_hugle
91761424a8d7        hello-world                        "/hello"                 2 weeks ago         Exited (0) 2 weeks ago                         focused_chatterjee
74bc5baaad36        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         gifted_knuth
5adb571f280a        c52dc19f7cb8                       "/bin/sh -c /start.sh"   2 weeks ago         Exited (1) 2 weeks ago                         nostalgic_kare
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ ### FART Main --- Ensure unused CONTAINERS are REMOVED / DELETED --- Its not enough just to remove the IMAGES 
dhankar@dhankar-VPCEB44EN:/media/dhankar/Dhankar_1/a2_18/a1____Tensor_Mar18/TensorServingDockerOwn$ 

