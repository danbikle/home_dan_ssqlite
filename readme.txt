~/ssqlite/readme.txt

The files in this dir were created on an ubuntu 14 host with these shell commands:

cd /home/dan/
mkdir tmp
mkdir ssqlite
cd tmp/
wget http://www.sqlite.org/2014/sqlite-autoconf-3080702.tar.gz
tar zxf sqlite-autoconf-3080702.tar.gz 
cd sqlite-autoconf-3080702/
./configure --prefix=/home/dan/ssqlite 
make
make install
cd /home/dan/ssqlite/
vi readme.txt
git init
git add .
git commit -am ssqlite_hello

Then, I installed the sqlite3 gem:

gem install sqlite3 -- --with-sqlite3-dir=/home/dan/ssqlite

dan@anaconda96 ~ $ 
dan@anaconda96 ~ $ gem install sqlite3 -- --with-sqlite3-dir=/home/dan/ssqlite
Building native extensions with: '--with-sqlite3-dir=/home/dan/ssqlite'
This could take a while...
Successfully installed sqlite3-1.3.10
1 gem installed
dan@anaconda96 ~ $ 
dan@anaconda96 ~ $ 
