# Setting up a project in craft #
## Follow these steps to set up a project in craft ##

1. Open your terminal and ensure that you are in the sites directory
2. Go to https://github.com/sophiebatten123/craft and clone this repository in the terminal
3. The name of the folder created in the sites directory is how you veiw the site e.g. if the folder is called practice_project you would go to practice_project.test
4. Open the project in VSCode and inside the terminal run composer install
5. Go to sequel ace and create a database in localhost by clicking the drop down then add database.
6. Create a .env file in the project and include the DBNAME used in sequel ace.
7. Run ./craft setup and follow the instructions (ensure that the siteurl is hhtp://practice_project.test/)
8. Login to the craft admin by going to practice_project.test/admin with the user name admin and the password what you just wrote in.

# Configuring ImageOptimize #
## Follow these steps to set up the plugin image optimize on your project ##

1. Within the CMS search for ImageOptimize and then install it on the project.
2. Copy the terminal command to also install it within the terminal.
3. Install the additional required packages using the command below:
    brew install webp
    npm install -g svgo                                                      
    brew install gifsicle
    brew install optipng
    brew install jpegoptim
4. Navigate to your vendor file and within nystudio107/craft-imageoptimize/src copy the config.php file and past it in your config file renaming it to image-optimize.php
5. Using the commands below update the paths in your image-optimize.php file and this should give green ticks on the plugin within the CMS
    which cwebp
    which gifsicle
    which optipng
    which jpegoptim
    which svgo
6. Inside the general.php file ensure you have updated the alliances so '@web' => 'http://craft.test/'.
7. When creating a volume for images this can then be used so @web/images/... and @webroot/images/...
8. Create a field called Image optimizer and then got to assets in settings and create a new volume, ensure that this field is included on the volume.
9. Create a field for asset and add it to the section you want to have an image. You should now be able to go to entries upload an image to the volume you want and this will optimize the image for you!

# Using Image Optimize #
## Follow this guide to use image optimize ##

1. When your image has been added to the entry you should now be able to access it in you .twig file!
2. First set the image to the entry field you need using {% set img = entry.image.one() %}
3. Now optimize the image using the optimizer that you have used in that volume where the image is set.
4. Then include the image optimized image src and srcset to make it responsive to screen sizes.

** Currently I am having to clear cache in the CMS and on the browser for this to show **

NOTE: Initially the images were not updating due to the route to the directly not correctly matching where the images are stored. Check this!
