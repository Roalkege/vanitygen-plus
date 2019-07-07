-----
Vanitygen PLUS! for Brocoin and Jumpcoin  
-----

-----
Getting Started  
-----  
**Download the latest binary from: https://github.com/exploitagency/vanitygen-plus/releases !**  
Linux Binary (Compiled on 64bit Debian Testing)  
Windows Binary (Compiled on Win10 64bit)  Will be added in the future

Extract the files,  
open a terminal/command prompt,  
change to directory containing vanitygen-plus binaries.  

Running On Linux: `./vanitygen -ARGS`, or `./oclvanitygen -ARGS`, `./keyconv -ARGS`, etc  

**For generating addresses using the CPU(slower) use: vanitygen !**

**NOTES:**	All arguments are case sensitive!  
	Address prefix must be at the end of the command.  
	oclvanitygen requires OpenCL and correct drivers.  

**Get a list of the supported Coins with:**  
Linux CPU: `./vanitygen -C LIST`  

A list of all the supported crypto coins will be output.  

Choose your coin from the list noting the ARGUMENT needed for the coin located in the left hand column.  
For LBRY it is simply LBRY.  For Bitcoin it is BTC.  Etc...  

**Now lets generate a BRO address with the prefix "BTEST":**  
Linux CPU: `./vanitygen -C BRO -o results.txt -i -k BTEST`

 * `-C BRO` : Chooses the BRO coin  
 * `-o results.txt` : saves the matches to results.txt  
 * `-i` : case-Insensitive(do not add this flag to match exact case)  
 * `-k` : keep going even after match is found(do not add this flag to stop after the first match)  
 * `BTEST` : the address you are searching for(BRO addresses start with "B")  


**If you have dependency errors on Linux  
or need instructions for compiling from source(Kaling Rolling/Linux) see link below:**  
https://legacysecuritygroup.com/index.php/projects/recent/12-software/35-oclvanitygen-compiling-and-use  

------  
Fix libcrypto.so.1.0.2 error(Debian, Ubuntu)  
------  
Error:
>./vanitygen: error while loading shared libraries: libcrypto.so.1.0.2: cannot open shared object file: No such file or directory  

Fix it by issuing the below commands, in turn either installing or downgrading libcrypto.  The error comes from an incompatibility with the newer version of libcrypto.  Most older projects have this same bug.  
```
wget http://ftp.us.debian.org/debian/pool/main/g/glibc/libc6-udeb_2.24-11+deb9u3_amd64.udeb
dpkg -i libc6-udeb_2.24-11+deb9u3_amd64.udeb
wget http://ftp.us.debian.org/debian/pool/main/o/openssl1.0/libcrypto1.0.2-udeb_1.0.2l-2+deb9u3_amd64.udeb
dpkg -i libcrypto1.0.2-udeb_1.0.2l-2+deb9u3_amd64.udeb
rm libc6-udeb_2.24-11+deb9u3_amd64.udeb && rm libcrypto1.0.2-udeb_1.0.2l-2+deb9u3_amd64.udeb 
```
Current List of Available Coins for Address Generation  
-----
|**Argument(UPPERCASE)** | **Coin** | **Address Prefix**  |
| --------------------------------------- | -------------------------------------------- | ------------ |
|42 | 42coin | 4  |
|AC | Asiacoin | A  |
|ACM | Actinium | N |
|AIB | Advanced Internet Block by IOBOND | A  |
|ANC | Anoncoin | A  |
|ARS | Arkstone | A  |
|ATMOS | Atmos | N  |
|AUR | Auroracoin | A  |
|AXE | Axe | P |
|BLAST | BLAST | B  |
|BLK | Blackcoin | B  |
|BRO | Brocoin | B  |
|BWK | Bulwark | b  |
|BQC | BBQcoin | b  |
|BTC | Bitcoin | 1  |
|TEST | Bitcoin Testnet | m or n  |
|BTCD | Bitcoin Dark | R  |
|CARE | Carebit | C  |
|CCC | Chococoin | 7  |
|CCN | Cannacoin | C  |
|CDN | Canadaecoin | C  |
|CLAM | Clamcoin | x  |
|CNC | Chinacoin | C  |
|CNOTE | C-Note | C |
|CON | PayCon | P  |
|CRW | Crown | 1  |
|DASH | Dash | X  |
|DEEPONION | DeepOnion | D  |
|DNR | Denarius | D  |
|DGB | Digibyte | D  |
|DGC | Digitalcoin | D  |
|DMD | Diamond | d  |
|DOGED | Doge Dark Coin | D  |
|DOGE | Dogecoin | D  |
|DOPE | Dopecoin | 4  |
|DVC | Devcoin | 1  |
|EFL | Electronic-Gulden-Foundation | L  |
|EMC | Emercoin | E  |
|EXCL | Exclusivecoin | E  |
|FAIR | Faircoin2 | f  |
|FLOZ | FLOZ | F  |
|FTC | Feathercoin | 6 or 7  |
|GAME | GameCredits | G  |
|GAP | Gapcoin | G  |
|GCR | Global Currency Reserve | G  |
|GRC | GridcoinResearch | R or S  |
|GRLC | Garlicoin | G  |
|GRN | GreenCoin | G  |
|GRS | Groestlcoin | F  |
|GRV | Gravium | G  |
|GUN | Guncoin | G or H  |
|HAM | HamRadiocoin | 1  |
|HBN | HoboNickels(and BottleCaps) | E or F  |
|HODL | HOdlcoin | H  |
|IC | Ignition Coin | i  |
|IXC | Ixcoin | x  |
|JBS | Jumbucks | J  |
|JIN | Jincoin | J  |
|JUMP | Jumpcoin | J  |
|KMD | Komodo (and assetchains) | R  |
|KORE | Kore | K  |
|LBRY | LBRY | b  |
|LEAF | Leafcoin | f  |
|LMC | LomoCoin | L  |
|LTC | Litecoin | L  |
|MGD | MassGrid | M  |
|MMC | Memorycoin | M  |
|MNC | Mincoin | M  |
|tMNC | Mincoin Testnet | m or n  |
|MNP | MNPCoin | M  |
|MOG | Mogwai | M  |
|MONA | Monacoin | M  |
|MUE | Monetary Unit | 7  |
|MYRIAD | Myriadcoin | M  |
|MZC | Mazacoin | M  |
|NEET | NEETCOIN | N  |
|NEOS | Neoscoin | S  |
|NLG | Gulden | G  |
|NMC | Namecoin | M or N  |
|NVC | Novacoin | 4  |
|NYAN | Nyancoin | K  |
|OK | OK Cash | P  |
|OMC | Omnicoin | o  |
|PIGGY | Piggycoin | p  |
|PINK | Pinkcoin | 2  |
|PIVX | PIVX | D  |
|PKB | Parkbyte | P  |
|PND | Pandacoin | P  |
|POT | Potcoin | P  |
|PPC | Peercoin | P  |
|PTC | Pesetacoin | K  |
|PTS | Protoshares | P  |
|QTUM | QTUM | Q  |
|RBY | Rubycoin | R  |
|RDD | Reddcoin | R  |
|RIC | Riecoin | R  |
|ROI | ROIcoin | R  |
|RVN | Ravencoin | R |
|SCA | Scamcoin | S  |
|SDC | Shadowcoin | S  |
|SKC | Skeincoin | S  |
|SPR | Spreadcoin | S  |
|START | Startcoin | s  |
|SXC | Sexcoin | R or S  |
|TPC | Templecoin | T  |
|TUX | Tuxcoin | T  |
|UIS | Unitus | U  |
|UNO | Unobtanium | u  |
|VIA | Viacoin | V  |
|VIPS | VIPSTARCOIN | V  |
|VPN | Vpncoin | V  |
|VTC | Vertcoin | V  |
|WDC | Worldcoin Global | W  |
|WKC | Wankcoin | 1  |
|WUBS | Dubstepcoin | D  |
|XC | XCurrency | X  |
|XPM | Primecoin | A  |
|YAC | Yacoin | Y  |
|YTN | Yenten | Y  |
|ZNY | BitZeny | Z  |
|ZOOM | Zoom coin | i  |
|ZRC | Ziftrcoin | Z  |

**If you found this repo useful, please consider a donation.  Thank You!**  

 * Donate Bitcoin: 1egacySQXJA8bLHnFhdQQjZBLW1gxSAjc  
