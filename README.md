# PABRIK CD

## Install perkakas
`$ sudo apt-get install git debootstrap genisoimage zsync`

## Setup GNUPG

## Menghajar Pabrik
* Buat User CDIMAGE  
`$ sudo adduser cdimage`

* Ubah CDIMAGE menjadi sudoers  
`$ sudo visudo -f /etc/sudoers`  
Tambahkan di baris terakhir dan simpan  
`cdimage ALL=NOPASSWD: ALL`

* Masuk Ke CDIMAGE  
`$ sudo su – cdimage`

* Menarik Skrip Pabrik CD  
`$ git clone github.com/tuanpembual/pabrik-cc.git`

* Ubah suai config pabrik  
`$ vim uluwatu.config`

* Mengatur debootstrap uluwatu  
`$ vim uluwatu.debootstrap`  
`$ sudo cp uluwatu.debootstrap /usr/share/debootstrap/scripts/uluwatu`

## Membuat Cetakan CD
`$ ./enter-cd-blankon.sh`

## Selamat Menikmati Error dan Baca Log

## Rilis
`$ sudo ./release-image -d /home/cdimage/images/livecd-harian/$DATE/ -r 11.0 -p /home/cdimage/images/rilis/uluwatu/Jahitan-XX/`
