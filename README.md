# Twig template system for Opencart 2.x

Because default template system sux.
Inspired by existing but deprecated solution: [vanderson139/opencart-twig](vanderson139/opencart-twig) - thanks buddy!

## Installation

1. composer require burdapraha/oc_twig master-dev
2. `composer require burdapraha/oc_twig dev-master`
3. Add this code to your composer.json project file:

```
    "scripts": {
        "post-install-cmd": [
            "php -r \"copy('vendor/burdapraha/oc_twig/vqmod/xml/twig.xml', 'upload/vqmod/xml/twig.xml');\""
        ],
        "post-update-cmd": [
            "php -r \"copy('vendor/burdapraha/oc_twig/vqmod/xml/twig.xml', 'upload/vqmod/xml/twig.xml');\""
        ]
    } 
```
    
It will move vqmod xml file to correct folder. If you are using another folder than "upload" for your document root, change these commands.

4. add constant `define('TWIG_CACHE', true);` to your config.php, /admin/config.php
5. optionally you can add row to your `.gitignore` file with path to tracy.xml (example: upload/vqmod/xml/twig.xml)
6. celebrate!