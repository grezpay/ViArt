ViArt

This plugin belongs to Grezpay payment gateway.

Introduction

This is the readme file for grezpay Payment Gateway Plugin Integration for ViArt Php based e-Commerce Websites. The provided Package helps store merchants to redirect customers to the grezpay Payment Gateway when they choose grezpay as their payment method. After the customer has finished the transaction they are redirected back to an appropriate page on the merchant site depending on the status of the transaction. The aim of this document is to explain the procedure of installation and configuration of the Package on the merchant website.

Installation

Unzip the files and copy paste the two folder "includes" and "payments" in viart root folder
Configuration

Log in to the ViArt Admin panel
In top Menu, from "Settings" click on "Payment Systems"
Click on "New Payments System"
Check "Is Active" option
Enter "Payment System Name"
In "Payment Url" fill "./payments/grezpay.php"
Choose "Form Submit Method" to "Post"
In Parameter List Section Add following Parameter with their values
Parameter name = Parameter Source[Parameter type]

invoice = order_id[variable]
item_name = basket[variable]
amount = order_total[variable]
email = email[variable]
channel = (type just a random number)[constant]
callback_url = [{site_url}order_final.php ][constant]
industry = (Name of your own choice)[constant]
merchant_id = (Provided by grezpay)[constant]
merchant_key = (Provided by grezpay)[constant]
merchant_website = (Provided by grezpay)[constant]
transaction_url = Url (For Testing Purpose | For Production Purpose)[constant]
name = name[variable]
phone = phone[variable]
Click on Save
Now from the payment gateway list, locate "grezpay" and click on "Final Checkout Page" Link
In Final Checkout Page link under validation parameters
Check "Additional Validation" checkbox
In "Validation Script" enter "./payments/grezpay_validate.php"
Set Order Success Status to "New Order"
Set Pending Status to "Pending"
Set Failure Status to "Failed"
In Final Messages Section , set the messages as per you need on thankyou page.
Click on Save.
grezpay PG URL Details
staging	
	Transaction Request URL     => https://uat.grezpay.com/crm/jsp/paymentrequest

Production
	Transaction URL             => https://merchant.grezpay.com/crm/jsp/paymentrequest
