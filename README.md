# bench-scripts

## vpsbench
https://github.com/mgutz/vpsbench - A script to run simple and comprehensive benchmarks on CPU and IO performance.

    $ bash <(wget --no-check-certificate -O - https://raw.github.com/mgutz/vpsbench/master/vpsbench)  

    Benching I/O ... OK
    Benching CPU. Bzipping 25MB file ... OK
    Benching inbound network. Downloading 100MB file ... OK
    Share at https://github.com/mgutz/vpsbench/wiki/VPS-Hosts
    CPU model:  Common KVM processor
    Number of cores: 6
    CPU frequency:  2399.998 MHz
    Total amount of RAM: 3011 MB
    Total amount of swap:  MB
    System uptime:   11 days, 2:04,       
    I/O speed:  910 MB/s
    Bzip 25MB: 4.22s
    Download 100MB file: 107MB/s

## nench
https://github.com/n-st/nench - A script loosely based on the established freevps.us/bench.sh. 

    $ (curl -s wget.racing/nench.sh | bash; curl -s wget.racing/nench.sh | bash) 2>&1 | tee nench.log  

    ------------------------------------------------
    nench.sh v2017.06.01 -- https://git.io/nench.sh
    benchmark timestamp:    2017-10-31 03:38:08 UTC
    -------------------------------------------------

    Processor:    Common KVM processor
    CPU cores:    6
    Frequency:    2399.998 MHz
    RAM:          2.9G
    Swap:         
    Kernel:       Linux 4.9.0-4-amd64 x86_64

    Disks:
    sda     30G  HDD

    CPU: SHA256-hashing 500 MB
     3.438 seconds
    CPU: bzip2-compressing 500 MB
     5.385 seconds
    CPU: AES-encrypting 500 MB
    3.174 seconds

    ioping: seek rate
    min/avg/max/mdev = 59.0 us / 180.1 us / 3.71 ms / 57.3 us
    ioping: sequential read speed
    generated 4.02 k requests in 5.00 s, 1005.5 MiB, 804 iops, 201.1 MiB/s

    dd: sequential write speed
    1st run:    810.62 MiB/s
    2nd run:    1144.41 MiB/s
    3rd run:    1239.78 MiB/s
    average:    1064.94 MiB/s

    IPv4 speedtests
    your IPv4:    x.x.x.x

    Cachefly CDN:         82.72 MiB/s
    Leaseweb (NL):        25.23 MiB/s
    Softlayer DAL (US):   6.94 MiB/s
    Online.net (FR):      21.97 MiB/s
    OVH BHS (CA):         97.26 MiB/s

    No IPv6 connectivity detected
    -------------------------------------------------

## serverkite - bench.sh 
https://serverkite.github.io - A aeronautic benchmarking script that handles speed test from 30+ datacenters and 20+ vps providers + I/O (Input / Output), ping, traceroute tests.

    $ git clone https://github.com/ServerKite/bench.sh.git && cd bench.sh && chmod +x bench.sh && bash bench.sh
    
## VPS Benchmark
http://busylog.net/vps-benchmark/ - Benchmark disk, cpu and network.

    wget http://busylog.net/FILES2DW/busytest.sh -O - -o /dev/null | bash
     __                          
    |__)    _  | _  _     _  _|_ 
    |__)|_|_)\/|(_)(_).  | )(-|_ 
         /     _/            
    http://busylog.net           
    -----------------------------
    busyupload.sh V0.1
    \|/
    This is a early version with learning purpose... check the TODO
    Some logs here: ftp_busy.log
    -----------------------------
    Check what we have installed here...
    openssl......installed (YES)
    wget.........installed (YES)
    ftp..........not installed (NO)
    ioping.......installed (YES)
    hdparm.......installed (YES)
    -----------------------------
    Network upload test....
    not performed tests.... test needs ftp and wget installed
    -----------------------------
    Test openSSL speeds (openssl signatures speed)....
    Doing 512 bit private rsa's for 10s: 160961 512 bit private RSA's in 10.00s
    Doing 512 bit public rsa's for 10s: 2403890 512 bit public RSA's in 10.00s
    Doing 1024 bit private rsa's for 10s: 59315 1024 bit private RSA's in 10.00s
    Doing 1024 bit public rsa's for 10s: 902191 1024 bit public RSA's in 10.00s
    Doing 2048 bit private rsa's for 10s: 7758 2048 bit private RSA's in 10.00s
    Doing 2048 bit public rsa's for 10s: 287012 2048 bit public RSA's in 10.00s
    Doing 3072 bit private rsa's for 10s: 2857 3072 bit private RSA's in 10.00s
    Doing 3072 bit public rsa's for 10s: 136506 3072 bit public RSA's in 10.00s
    Doing 4096 bit private rsa's for 10s: 1267 4096 bit private RSA's in 10.01s
    Doing 4096 bit public rsa's for 10s: 78697 4096 bit public RSA's in 10.00s
    Doing 7680 bit private rsa's for 10s: 139 7680 bit private RSA's in 10.05s
    Doing 7680 bit public rsa's for 10s: 23533 7680 bit public RSA's in 10.00s
    Doing 15360 bit private rsa's for 10s: 26 15360 bit private RSA's in 10.29s
    Doing 15360 bit public rsa's for 10s: 6285 15360 bit public RSA's in 10.00s
    OpenSSL 1.1.0f  25 May 2017
    built on: reproducible build, date unspecified
    options:bn(64,64) rc4(8x,char) des(int) aes(partial) blowfish(ptr) 
    compiler: gcc -DDSO_DLFCN -DHAVE_DLFCN_H -DNDEBUG -DOPENSSL_THREADS -DOPENSSL_NO_STATIC_ENGINE -DOPENSSL_PIC -DOPENSSL_IA32_SSE2 -DOPENSSL_BN_ASM_MONT -DOPENSSL_BN_ASM_MONT5 -DOPENSSL_BN_ASM_GF2m -DSHA1_ASM -DSHA256_ASM -DSHA512_ASM -DRC4_ASM -DMD5_ASM -DAES_ASM -DVPAES_ASM -DBSAES_ASM -DGHASH_ASM -DECP_NISTZ256_ASM -DPADLOCK_ASM -DPOLY1305_ASM -DOPENSSLDIR="\"/usr/lib/ssl\"" -DENGINESDIR="\"/usr/lib/x86_64-linux-gnu/engines-1.1\"" 
                  sign    verify    sign/s verify/s
    rsa  512 bits 0.000062s 0.000004s  16096.1 240389.0
    rsa 1024 bits 0.000169s 0.000011s   5931.5  90219.1
    rsa 2048 bits 0.001289s 0.000035s    775.8  28701.2
    rsa 3072 bits 0.003500s 0.000073s    285.7  13650.6
    rsa 4096 bits 0.007901s 0.000127s    126.6   7869.7
    rsa 7680 bits 0.072302s 0.000425s     13.8   2353.3
    rsa 15360 bits 0.395769s 0.001591s      2.5    628.5
    -----------------------------
    Disk seek rate test (ioping)....
    
    --- . (ext4 /dev/sda1) ioping statistics ---
    14.9 k requests completed in 2.96 s, 58.4 MiB read, 5.06 k iops, 19.8 MiB/s
    generated 15.0 k requests in 3.00 s, 58.4 MiB, 4.98 k iops, 19.5 MiB/s
    min/avg/max/mdev = 61.9 us / 197.8 us / 5.88 ms / 97.4 us
    -----------------------------
    Direct (not cached) disk reads (hdparm)....
    Test disk /dev/sda1
    
    /dev/sda1:
    Timing O_DIRECT disk reads: 3624 MB in  3.00 seconds = 1207.86 MB/sec
    
## bench.sh
https://bench.sh - view system information and test the network, disk of your Linux server.

    $ wget -qO- bench.sh | bash
    
    ----------------------------------------------------------------------
    CPU model            : Common KVM processor
    Number of cores      : 6
    CPU frequency        : 2399.998 MHz
    Total size of Disk   : 28.5 GB (2.2 GB Used)
    Total amount of Mem  : 3011 MB (631 MB Used)
    Total amount of Swap : 3068 MB (0 MB Used)
    System uptime        : 11 days, 3 hour 10 min
    Load average         : 0.01, 0.11, 0.09
    OS                   : Debian GNU/Linux 9
    Arch                 : x86_64 (64 Bit)
    Kernel               : 4.9.0-4-amd64
    ----------------------------------------------------------------------
    I/O speed(1st run)   : 872 MB/s
    I/O speed(2nd run)   : 1.2 GB/s
    I/O speed(3rd run)   : 1.2 GB/s
    Average I/O speed    : 1109.9 MB/s
    ----------------------------------------------------------------------
    Node Name                       IPv4 address            Download Speed
    CacheFly                        205.234.175.175         106MB/s       
    ...
    ----------------------------------------------------------------------

