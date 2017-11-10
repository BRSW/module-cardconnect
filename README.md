# CardConnet Lite for Magento 2
CardConnet Lite is a secure payment gateway for Magento. The Customer Information Manager (CIM) function provides tokenization of customer payment information. It stores this information on secure servers, simplifying PCI compliance. Instead of storing sensitive customer information on a local server, it is stored on CardConnet’s secure servers.

Magento CardConnet Lite extensions combine the powerful features of the CIM service with the selling power of the Magento platform. It is a fast and simple way to add the payment security and convenience of the CardConnet.

- 100% PCI Compliant - card data is never stored on your server
- Secure payments and customer information storage
- Decreases checkout time
- Authorization/capture
- Refund

## Installation with composer

```bash
cd <magento_root>
composer config repositories.blackridgesoftware/module-cardconnect vcs git@github.com:brsw/module-cardconnect.git
composer require brsw/module-cardconnect
php bin/magento --clear-static-content module:enable Brsw_CardConnect
php bin/magento setup:upgrade
php bin/magento cache:flush 
```

## Installation without composer
* Download zip file of this extension
* Place all the files of the extension in your Magento 2 installation in the folder app/code/Brsw/CardConnect
* Enable the extension: `php bin/magento --clear-static-content module:enable Brsw_CardConnect`
* Upgrade db scheme: `php bin/magento setup:upgrade`
* Clear cache


## Configuration
You may configure your gateway settings in Magento admin panel.
Stores -> Settings -> Configuration -> Sales -> Payment methods -> Other payment methods -> Card Connect Gateway

![0001](https://user-images.githubusercontent.com/32928153/32607647-59db646e-c562-11e7-9d16-de4cf79fe804.png)
Next, fill all necessary fields, save configuration and flush Magento cashe.

## User journey
Select and add a product to cart then go to checkout
![0002](https://user-images.githubusercontent.com/32928153/32607648-59fd626c-c562-11e7-8bcb-770fa3ae697c.png)

After filling the information about shipment method and address details user will go to payment page.
Here customers need to input their card data and press “Place order” button.
![0003](https://user-images.githubusercontent.com/32928153/32607649-5a194d92-c562-11e7-869b-04d920060aa8.png)

---
[![Alt text](https://blackridgesoftware.com/media/logo/default/brsw_logo.png "BlackRidge Software")](https://blackridgesoftware.com/)