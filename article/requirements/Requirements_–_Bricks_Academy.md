# Requirements – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/requirements/](https://academy.bricksbuilder.io/article/requirements/)  
**Last Updated:** 2025-05-22T19:59:04.510Z  
**Extracted:** 2025-05-31 16:56:43

---

# Requirements – Bricks Academy

To provide you with a cutting-edge site builder for WordPress Bricks uses the most modern technology stack (VueJS 3, etc.) while keeping sufficient backward compatibility.

Below are a few minimum requirements your server should meet so Bricks runs smoothly:

*   PHP 7.4+
*   MySQL 5.6+
*   WordPress memory limit of at least 64 MB
*   Max file upload size of at least 16 MB
*   Modern browser: **Please use the latest version of Chrome, Firefox, Safari, or Microsoft Edge when editing your website with Bricks**. Older browsers (e.g. Internet Explorer) lack support for some of the more advanced builder features.

_Bricks is a self-hosted solution that you download & install on your own WordPress website!_

## How To Increase WP Memory Limit

You can define **WP\_MEMORY\_LIMIT** by adding the following code to your **wp-config.php** file (above the “That’s all, stop editing!” line):

define( 'WP\_MEMORY\_LIMIT', '256M' );
/\* That's all, stop editing! Happy publishing. \*/

Some web hosts set the PHP memory limit to 8 MB. In that case, you might consider upgrading to a more powerful hosting plan. If your host does not allow you to config this setting by yourself, please get in touch with them.

## How To Increase Max File Upload Size

If you encounter problems uploading larger files to your site (or when downloading high-resolution images from Bricks’ Unsplash integration) there are a few ways to increase the maximum upload file size.

A maximum upload size of 16 MB should suffice. But 64 MB would be ideal. Log into your hosting account and change the following two **PHP server settings** to:

*   post\_max\_size: 64M
*   upload\_max\_filesize: 64M

If you have access to your **php.ini** file, located in the root directory of your WordPress installation, open it, and modify the following settings:

upload\_max\_filesize \= 64M
post\_max\_size \= 64M

You can also add the following code to your **.htaccess** file, but make sure to backup your existing .htaccess file beforehand:

php\_value upload\_max\_filesize 64M
php\_value post\_max\_size 64M

If all above fails, you can try adding the following code to your wp-config.php:

@ini\_set( 'upload\_max\_size' , '64M' );
@ini\_set( 'post\_max\_size', '64M');

To confirm that your maximum upload file size has been updated successfully, go to **Media > Add New**. On the bottom of this page, you should see your maximum upload file size.

## How To Increase Maximum Execution Time

When you start seeing a message like “Maximum execution time of 30 seconds exceeded” you have to increase the execution time of your website by using one of the following three solutions:

**#1: Add the following code to your wp-config.php file (above the “That’s all, stop editing!” line):**

set\_time\_limit(180);
/\* That's all, stop editing! Happy publishing. \*/

**#2: Backup your .htaccess file and add the following code to it:**

php\_value max\_execution\_time 180

**#3: Add the following code to your php.ini file:**

max\_execution\_time \= 180

---

*This documentation was extracted from the database for URLs containing 'bricks'*
