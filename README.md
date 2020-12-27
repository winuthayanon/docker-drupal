# docker-drupal
# How to install
git clone https://github.com/winuthayanon/docker-drupal
cd docker-drupal
# edit file .env

sudo chown www-data.www-data -R ./data/sites/default/*

# edit file in data/sites/default/settings.php 
uncomment line 717-719
$settings['trusted_host_patterns'] = [
       'drupal.yourdomain.com',
];

# start by this command-line
docker-compose up -d
# stop by this command-line
docker-compose down

# go to https://drupal.yourdomain.com/ to install
# Good luck!
