# centosconfig



# init 

sudo yum update

sudo yum upgrade

sudo dnf update 


#  Step 1 – Install Nginx
sudo dnf install nginx

sudo systemctl enable nginx

sudo systemctl start nginx



# Add EPEL and REMI repositories
# Add the EPEL and REMI repositories which has PHP 7.4 package and other required PHP extensions.


sudo yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

sudo yum -y install https://rpms.remirepo.net/enterprise/remi-release-8.rpm


sudo dnf -y install dnf-utils


sudo dnf module install php:remi-7.4




# Install PHP 7.4 Extensions


sudo yum install -y php-dom php-simplexml php-ssh2 php-xml php-xmlreader php-curl php-date php-exif php-filter php-ftp php-gd php-hash php-iconv php-json php-libxml php-pecl-imagick php-mbstring php-mysqlnd php-openssl php-pcre php-posix php-sockets php-spl php-tokenizer php-zlib


sudo dnf install  php-fpm  php-gd php-mysqlnd



# to test actual php version run this command : 

php -v

# activiting php fpm 

sudo systemctl enable php-fpm

sudo systemctl start php-fpm
