#drupal_commerce2.*

Integration instructions:
 you will need a working Drupal 8 with the latest version of Drupal Commerce 2 installed.

add the following to your composer.json under repositories:

"repositories": [
    {
      "type": "package",
      "package": {
        "name": "payfast",
        "version": "2.3.0",
        "type": "drupal-module",
        "source": {
            "url": "https://github.com/stewest/commerce_payfast.git",
            "type": "git",
            "reference": "2.3.0"
          }
      }
    }

and then:

"extra": {
  "installer-paths": {
    "web/modules/contrib/commerce/modules/{$name}": [
      "payfast"
    ],
  }
}


Depends on your module folder path root/web/modules... or root/modules...

OR if you're not using composer.

1. Unzip and copy the payfast folder to the ../modules/contrib/commerce/modules/ folder so that the path is ../modules/contrib/commerce/modules/payfast.

2. Log into the admin dashboard and install Commerce PayFast on the 'Extend' page.

3. Navigate to Commerce>Configuration>Payments and click on 'new payment gateway'

4. Select PayFast and configure as required.

5. Click Save.
