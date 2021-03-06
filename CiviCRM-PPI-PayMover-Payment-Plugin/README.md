CiviCRM-PPI-PayMover-Payment-Plugin
================================

Description
-------------------------
Adds the PayMover Payment processor to CiviCRM

Requirements
-------------------------
Webserver (Apache/Ngix/etc.)
-- With SSL
PHP 5.x.x
-- With cURL
-- With SSL
CiviCRM - Tested on 3.4.8
PayMover Libraries - Tested with PPI PayMover Version 12.10.0


Setup
-------------------------
Run this MySQL command on your CiviCRM database (Check that the id is correct, here I used 16:
INSERT INTO `civicrm_payment_processor_type` (`id`, `name`, `title`, `description`, `is_active`, `is_default`, `user_name_label`, `password_label`, `signature_label`, `subject_label`, `class_name`, `url_site_default`, `url_api_default`, `url_recur_default`, `url_button_default`, `url_site_test_default`, `url_api_test_default`, `url_recur_test_default`, `url_button_test_default`, `billing_mode`, `is_recur`, `payment_type`) VALUES (16, 'PayMover', 'PPI PayMover', NULL, 1, 0, 'Token', NULL, NULL, NULL, 'Payment_PayMover', NULL, 'https://etrans.paygateway.com/TransactionManager/index.php', NULL, NULL, NULL, 'https://etrans.paygateway.com/TransactionManager/index.php', NULL, NULL, 1, 0, 1);

Place your PPI PayMover PHP files in <web root>/sites/all/modules/civicrm/packages/
Place PayMover.php in <web root>/sites/all/modules/civicrm/CRM/Core/Payment/

-- IMPORTANT --
Change the token in PayMover.php to the token you recieved from PayMover.  Add TEST in front to make it a test token.

Notes
-------------------------
The payment processor can now be enabled in the usual way through the CiviCRM interface.

Author
-------------------------
Craig Vanderlinden
    Drupal.org - VanD
    Twitter - cvanderlinden
    Website - cvanderlinden.com