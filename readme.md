# Drupal Sample Project

## 1. Installation mit Composer
fin rc --image=docksal/cli:2.13-php7.4 composer create-project drupal/recommended-project softlevel

### 2. Einrichten docksal

### 3. Die Settings.php
### 4. Composer Pitfals.
// Patches über composer
fin exec composer require cweagans/composer-patches
// npm / bower libraries
fin exec composer require oomphinc/composer-installers-extender

fin exec composer require drush/drush --dev

fin exec composer require drupal/MODULE_NAME
#### Composer upate / composer.lock.
#### Patches
### 5. Config export / Config import
#### Workflow
``` 
drush cex
git add .
git commit -a -m "...."
git pull 
drush cim
```
### 6. config split
$config['config_split.config_split.local']['status'] = TRUE;


### 7. Häufige drush Befehle
* Cache leeren: `drush cr` 
* Konfiguration exportieren: `drush cex` 
* Konfiguration importieren: `drush cim` 
* Als admin anmelden: `drush uli` 


### 8. Drupal console

### 9. Deployment

### Anhang
  "repositories": {
    "asset-packagist": {
      "type": "composer",
      "url": "https://asset-packagist.org"
    },
   
    "drupal": {
      "type": "composer",
      "url": "https://packages.drupal.org/8"
    },
  },
  
  
  ```
"installer-types": [
    "bower-asset",
    "npm-asset",
    "test"
],
        
```
```
"web/libraries/{$name}": [
    "type:drupal-library",
    "type:npm-asset",
    "type:bower-asset"
],
```

``` 
        "patches": {
            "drupal/core": {
                "Fix broken theme suggestions for views.": "https://www.drupal.org/files/issues/2020-11-23/2118743-190.patch"
            }
        },
``` 

