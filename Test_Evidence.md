# My Favourite Recipes Test Evidence
## Unit and Functional Testing

####    Navigation
The navigation bar is consistent across all pages and device sizes.
#####   Main Nav Bar before logged in
 ![image](static/documentation_files/images/nav_bar_large.png)
#####   Main Nav Bar after logged in
 ![image](static/documentation_files/images/nav_bar_logged_in.png)
#####   Hamburger Nav Bar on smaller devices
 ![image](static/documentation_files/images/unit_testing_images/nav_bar_medium.png)
#####   Side Nav Bar on smaller devices
 ![image](static/documentation_files/images/nav_side_bar_meduim.png)

Each of the navigation links takes the webiste user to the relavent pages.

####    Footer
The footer allows for the addition of information and links to sites that are not directly part of this site. The website user can find information about the creator of this site. In the real world these links would be for other company information including corporate social media. The website user has access to be able to contact the owner of the site via the **contact us** link.

#####   Footer on Large Devices
 ![image](static/documentation_files/images/unit_testing_images/footer_larger.png)
#####   Footer on Medium Devices
 ![image](static/documentation_files/images/unit_testing_images/footer_medium.png)
#####   Footer on Small Devices
 ![image](static/documentation_files/images/unit_testing_images/footer_small.png)
####    Github
The link to Github opens in a separate window.

 ![image](static/documentation_files/images/unit_testing_images/github.png)
####    LinkedIn
The link to LinkedIn opens in a separate window.

 ![image](static/documentation_files/images/unit_testing_images/linkedin.png)
####    Facebook
The link to Facebook opens in a separate window.

 ![image](static/documentation_files/images/unit_testing_images/facebook.png)
####    Instagram
The link to Instagram opens in a separate window.

 ![image](static/documentation_files/images/unit_testing_images/instagram.png)
####    Twitter
The link to Twitter opens in a separate window.

 ![image](static/documentation_files/images/unit_testing_images/twitter.png)


#####   Materialize Parallax Image
######    Issues
There is an issue when moving between device sizes where the home page, parallax image does not cover the whole of the container.

 ![image](static/documentation_files/images/unit_testing_images/home_small_issue.png)

I tried to fix this by removing some of the CSS styling for the .parallax-container class so that it only contained the overlay to lighten the image which enabled the materialize CSS. Although this looked like it worked initially, when I reloaded and ran some more tests the issue stayed the same.
######    Resolutions
After much investigation I have come to the conclusion this is an intermittent issue with the materializecss styling for the parallax class. I thought it was related to the carousel I have on top of the background image but found I have the same issue on other pages where there is no background image. something happens to change the element.style but I have not been able to uncover the exact issue.

 ![image](static/documentation_files/images/unit_testing_images/home_parallax_image_styling.png)
 ![image](static/documentation_files/images/unit_testing_images/parallax_issue_after_refresh.png)
 ![image](static/documentation_files/images/unit_testing_images/parallax_issue.png)
 ![image](static/documentation_files/images/unit_testing_images/add_category_parallax_styling.png)

####    Home Page
######   Issues
There is a strange issue with the home page where by when the site is opened on a desktop and all navigation is done on that resolution the navigation bar fits the whole window and there is no horizontal scroll bar.
 ![image](static/documentation_files/images/unit_testing_images/home_large.png)
If the same page is inspected using DevTools and then DevTools is closed a horizontall scroll bar appears.
######    Resolutions
 ![image](static/documentation_files/images/unit_testing_images/home_large_issue.png)
To fix the issue I had to add some styling for the `.nav-extended` class to force the bar to being the full width and then had to add some padding to the right of the ul element so that all them navigation options were still visible.

####    About Page
The about page has no functionality to test but the format for UX needs to be validated across all device sizes.
######   Issues
There is an issue with white space on either side of the about container.
 ![image](static/documentation_files/images/unit_testing_images/about_large_issue.png)
######    Resolutions
This issue occured because the class container is a materialize class which has a set width that is smaller than the full view width of a screen. By changing the classes from .container .about to .container-about in both the HTML and CSS the issue is resolved.
 ![image](static/documentation_files/images/about_large_fixed.png)

####    Getting Started Page
The getting started page has one button which allows the website user to register with the site to allow them to add their own recipes. This button works.

 ![image](static/documentation_files/images/getting_started_large.png)

####    Recipes Page
The recipe page will grow in length as more recipes are added. Clicking on one of the recipe cards will take the website user to the recipe detail page. Each recipe shows how many people have liked or disliked each recipe. 
#####   Recipes Page Large
 ![image](static/documentation_files/images/recipes_page_large.png)
#####   Recipes Page Medium
 ![image](static/documentation_files/images/unit_testing_images/recipes_page_medium.png)
#####   Recipes Page Small
 ![image](static/documentation_files/images/unit_testing_images/recipes_page_small.png)

The recipe card page allows the website user to search recipes for specific categories. Here I used the word fun 

![image](static/documentation_files/images/unit_testing_images/fun_filter.png) which brought back only one recipe 

![image](static/documentation_files/images/unit_testing_images/recipe_card_filter.png)

If a recipe is loaded without an image, the site provides a default image.

![image](static/documentation_files/images/unit_testing_images/recipe_card_default_image.png)
######   Issues
1. When an image is uploaded it will need to be resized so that when it is displayed the image does not pull out of shape.
2. If there is no image a default image is needed and the recipe title font colour will need to darken.
######    Resolutions
1. Using google to search for resizing of images using Python I found [auth0.com](https://auth0.com/blog/image-processing-in-python-with-pillow/#Resizing-Images)
2. Added default image code to HTML and added a new class with CSS to change the recipe title from white to brown so that it can be read.
 ![image](static/documentation_files/images/unit_testing_images/recipe_cards.png)
####    Register Page
The website user needs to register to be able to add any new recipes or categories which they will subsequently be able to read, change or delete later.

 ![image](static/documentation_files/images/register_large.png)
####    Log-in Page
Once the website user has an account they can log in and will then have access to add, change, delete recipes and add, change categories.

 ![image](static/documentation_files/images/login_large.png)
####    Log-out
Logging out take the website user back to the login page.
###     Profile Page
When a website user has created an account and/or logged in they are taken to the profile page where they have full access to their account and recipes with only add and change access to their categories.
 ![image](static/documentation_files/images/profile_large.PNG)
######   Issues
The text on the buttons on the profile card are truncated.
######    Resolutions
I increased the button width from 12rem to 14rem.
From this page a website user can change their password, delete their account (which will delete all the recipes they have created), add a new recipe, maintain categories. When the website user has added some recipes, a table is displayed detailing the recipes they have added. Clicking on the recipe name will take them to a read-only view of the recipe or they can click on the maintain recipe button to change or delete the recipe.

#####   Recipe Table
The recipes table scrolls horizontally on medium and small devices and vertically on large devices.
######  large
![image](static/documentation_files/images/profile_large.PNG)
######  small
 ![image](static/documentation_files/images/unit_testing_images/profile_scroll_small.png)

####    Display Recipe Page
This page shows all the details of the recipe so that the website user can cook it easily. The website user can also like or dislike the recipe.
![image](static/documentation_files/images/unit_testing_images/recipe_details.png)

If the website user has already liked or disliked the recipe, a flash message is displayed and they cannot like/dislike it again.

![image](static/documentation_files/images/unit_testing_images/already_liked.png)
#####    Issues
1. The the liked button was clicked but the website user was not logged-in the site crashed. This is because session does not have a user element unless a visitor is logged in. 
![image](static/documentation_files/images/like_issue_no_account.png)
######   Resolution
I changed the code to include a test to check session for a user element. This has the effect of not allowing anyone who does not have an account from liking or disliking the recipes.

![image](static/documentation_files/images/like_issue_fix.png)

After some thought I decided the site would be more efficient if I made the change in the HTML. This would reduce the processing time of reloading the page. I changed the HTML to display two different types of buttons depending on whether the website visitor was logged-in or not. 

![image](static/documentation_files/images/unit_testing_images/recipe_html.png) 

I also changed the CSS to fix the alignment using flex-box on both the recipe detail and the recipe card pages.

 ![image](static/documentation_files/images/unit_testing_images/flex_rating.png) 
 ![image](static/documentation_files/images/unit_testing_images/recipe_ratings.png) 
 ![image](static/documentation_files/images/unit_testing_images/flex_score.png) ![image](static/documentation_files/images/unit_testing_images/recipe_buttons.png)

####    Add Recipe Page
![image](static/documentation_files/images/add_recipe.png)

If the website user wants to load an image, this needs to be done before the recipe details are filled in because the site currently loses all the other information when the upload button is pressed. The website use can change the recipe and upload an image then.
#####   Upload image
![image](static/documentation_files/images/unit_testing_images/upload_image.png)
When the website user has chosen the image, they want to use from the personal collection of images (or one they have downloaded) and clicked the upload button, an image is loaded to cloudinary and a new recipe record with the url is created in the recipe collection in MongoDB.
![image](static/documentation_files/images/unit_testing_images/upload_banana.png)
![image](static/documentation_files/images/unit_testing_images/cloudinary.png)
![image](static/documentation_files/images/unit_testing_images/mongobd_image.png)
######   Issues
1. When entering the title of the recipe it did not allow an apostrophe.
![image](static/documentation_files/images/unit_testing_images/add_recipe_issue.png)
2. The 3 larger fields are `<textareaa>` elements which do not have the `pattern` attribute and will therefore allow any character. This is a risk because a hacker could easily enter lines of code that could cause serious damage to the database.
![image](static/documentation_files/images/unit_testing_images/textarea.png) 
######   Resolution
1. I modified the pattern on the input element `pattern="([^\s][A-z0-9À-ž&;,.'\s]+)" `
![image](static/documentation_files/images/unit_testing_images/add_recipe_fix.png)
2. Although `<textarea>` feels like the correct type of element, to keep the database secure using the minimum amount of code I changed the elements `<input type="text"` and applied the above pattern. With more time I could potentially use some javascript keystroke listeners to test each character entered but I beleive that may impact response time.
![image](static/documentation_files/images/unit_testing_images/text_input.png)

####    Edit Recipe Page
This page looks almost identical to the Add Recipe page.

![image](static/documentation_files/images/edit_recipe.png)
######   Issues
1. When entering the temperature, "N/A" is not allowed but if the recipe does not need cooking not applicible is more appropriate than zero.
![image](static/documentation_files/images/unit_testing_images/pattern_na_issue.png)
2. When adding the chocolate conflake buns recipe I wanted to put brackets around the "milk or dark chocolate" but this was not allowed with the pattern. The `Please match requested format` message appeared
######   Resolution
1. I modified the pattern on the input elements pattern to allow "N/A" for numbers`pattern="([^\s][0-9N/A]+)" `
![image](static/documentation_files/images/unit_testing_images/pattern_na_fix.png)
2.  I modified the pattern on the input elements pattern to allow brackets for the text type`pattern="([^\s][A-z0-9À-ž&;,./()'\s]+)" `

####    Manage Categories Page
The add category page is very simple and I could not find any issues.

 ![image](static/documentation_files/images/categories_not_admin.png)
#####   Delete Category
Only "admin" has access to delete categories on the Manage Category Page. On the below image the category "Test Cat1" can be seen.
![image](static/documentation_files/images/unit_testing_images/delete_cat_screen.png)
This image shows a recipe with the category "Test Cat1" in MongoDB.

![image](static/documentation_files/images/unit_testing_images/delete_cat_mongdb.png)

If '"admin" tries to delete this message they recieve a flash message telling them a recipe is using that category and the category is not deleted.
![image](static/documentation_files/images/unit_testing_images/delete_cat_no_message.png)
When a category is not attached to a recipe "admin" can delete it and a confirmation message will be displayed.
![image](static/documentation_files/images/unit_testing_images/delete_cat_success_message.png) 

####    Add Category Page
The add category page is very simple and I could not find any issues.
![image](static/documentation_files/images/add_category.png)
If the website user tries to add a duplicate category they see a flash message and the systems stops them.
![image](static/documentation_files/images/unit_testing_images/add_cat_message_exist.png)

####    Edit Category Page
The update category page is very simple and I could not find any issues.
 ![image](static/documentation_files/images/edit_category.png)

####    Contact Us Page
The below screen shots show the information pertaining to a message being created on the website via the contact us page.
![image](static/documentation_files/images/unit_testing_images/test_contact_us.png)
It arriving in the designated email folder
![image](static/documentation_files/images/unit_testing_images/email_received.png)
And a confirmation email being recieved by the email address on the above screen shot
![image](static/documentation_files/images/unit_testing_images/email_received.png)

##  Lighthouse Testing
###     Home
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/home_desk.png)
![image](static/documentation_files/images/lighthouse_images/home_desk_best_practice.png)
1. The links to my social media pages on `base.html` have the attribute `target="_blank"` which lighthouse says can "expose your site to performance and security issues". 
I have added `rel="noopener"` which should avoid the issues.
![image](static/documentation_files/images/lighthouse_images/home_desk_SEO.png)
1. There was no meta data wo I added.
2. The `href` on the `a` tag for the brand logo was missing it's `#`
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/home_desk_after.png)
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/home_mobile.png)
I adjusted the size of the images which improved the scores a bit. I also tried various "lazy load" API's namely AMP and Magneto as suggested by Chrome but they made the stats worse so I have decided to leave the images as they are.
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/home_mobile_after.png)
###     Recipes
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/recipes_desk.png)
There were some minor changes made such as the colour of the font on the reset button, adding a label with a visible font colour to the search bar and changing the Category on the cards from`<h5>` to `<span>` elements.
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/recipes_desk_after.png)
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/recipes_mobile.png)
The changes made to the desktop version improved the mobile version
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/recipes_mobile_after.png)
###     Register
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/register_desk.png)
This test gave all green lights and while improvements could be made, they are not necessary.
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/register_mobile.png)
This test gave all green lights and while improvements could be made, they are not necessary.
###     Login
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/login_desk.png)
This test gave all green lights and while improvements could be made, they are not necessary.
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/login_mobile.png)
This test gave all green lights and while improvements could be made, they are not necessary.
###     Profile
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/profile_desk.png)
I tried to improve the 'Best practice' test by modifying some of the image sizes and played with the aspect ratio. In the end I added a `profile-image`class and didn't use any of the aspect suggestions because I wanted the profile image to be a circle and everything I tried made it an oval which altered the rest of the layout of the card.
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/profile_desk_after.png)
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/profile_mobile.png)
Chrome warning 

![image](static/documentation_files/images/lighthouse_images/chrome.png)
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/profile_mobile_after.png)
Testing the site under incognito did make some improvements but the security highlighted by lighthouse is directly related to Heroku. The site is accessed using HTTP instead of HTTPS, the more modern and more secure version of HTTP.
![image](static/documentation_files/images/lighthouse_images/profile_incog.png)
###     Change Password
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/change_password_desk.png)
This test gave all green lights and while improvements could be made, they are not necessary.
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/change_password_mobile.png)
Chrome warning 

![image](static/documentation_files/images/lighthouse_images/chrome.png)
#####   Final Test Results
Testing this page in incoginito improved the performance but failed on security of the site being hosted viar Heroku on HTTP.
![image](static/documentation_files/images/lighthouse_images/change_password_incog.png)
###     Recipe Detail
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/recipe_detail_desk.png)
I removed the parallax background image and changed it to the colour "whitesmoke"
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/recipe_detail_desk-after.png)
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/recipe_detail_mobile.png)
The issues are mostly related to the imported styling and scripts with the exception of the image imported from Cloudingary. 
###     Add Recipe
####    Desktop
#####   Initial Test Results
Before running the test, I removed the background image
![image](static/documentation_files/images/lighthouse_images/add_recipe_desk.png)
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/add_recipe_mobile.png)
The issues are mostly related to the imported styling and scripts. 
#####   Final Test Results
Testing in incognito mode improved the performance of the site
![image](static/documentation_files/images/lighthouse_images/add_recipe_incog.png)
###     Edit Recipe
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/edit_recipe_desk.png)
I removed the parallax background image and changed it to the colour "whitesmoke"
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/edit_recipe_desk_after.png)
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/edit_recipe_mobile.png)
The issues are mostly related to the imported styling and scripts with the exception of the image imported from Cloudingary. 
#####   Final Test Results
![image](static/documentation_files/images/lighthouse_images/edit_recipe_mobile_after.png)
###     Manage Categories
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/manage_cats_desk.png)
This test gave all green lights and while improvements could be made, they are not necessary.
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/manage_cats_mobile.png)
The issues are mostly related to the imported styling and scripts
###     Add Category
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/add_cat_desk.png)
This test gave all green lights and while improvements could be made, they are not necessary.
####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/add_cat_mobile.png)
Chrome warning

![image](static/documentation_files/images/lighthouse_images/chrome.png)
#####   Final Test Results
Testing this page in incoginito improved the performance but failed on security of the site being hosted viar Heroku on HTTP.
![image](static/documentation_files/images/lighthouse_images/add_cat_incog.png)
###     Edit Category
####    Desktop
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/edit_cat_desk.png)
This test gave all green lights and while improvements could be made, they are not necessary.

####    Mobile
#####   Initial Test Results
![image](static/documentation_files/images/lighthouse_images/edit_cat_mobile.png)
Chrome warning 

![image](static/documentation_files/images/lighthouse_images/chrome.png)
#####   Final Test Results
![image](Testing this page in incoginito improved the performance but failed on security of the site being hosted viar Heroku on HTTP.
![image](static/documentation_files/images/lighthouse_images/edit_cat_incog.png))


## User Story Testing
### User Experience
######  User Story 1:   Recipe Details
**As a** visitor, 
**I want** to find some tasty and fun recipes
**So that** I can quickly and easily bake something tasty for family and friends
**Given** a visitor is interested in baking,
**When** they visit the site and open a recipe,
**Then** the recipe should have all the information needed to create the dish and be clear and easy to follow.
######  Results
As soon as a visitor opens the website images of available recipes are displayed in a carousel which they can scroll through to find something that looks tasty to bake or the second option on the navigation menu takes the visitor to a page containing all the recipes where they can reduce the number of recipes by entering a category or some word in the categories.

*Click on the recipe image to be taken to the recipe detail*

![image](static/documentation_files/images/user_story_images/us1_carousel.png)

*Click on the menu option "Recipes" to be taken to the recipe card page*

![image](static/documentation_files/images/user_story_images/us1_menu.png)

*Click on the recipe card to be taken to the recipe detail*

![image](static/documentation_files/images/user_story_images/us1_recipes.png)

*The recipe detail has all the information need to cook the recipe*

![image](static/documentation_files/images/user_story_images/us1_recipe_detail.png)
######  User Story 2:   Favourites
**As a** visitor, 
**I want** to know if other people like the recipe
**So that** I am confident I will enjoy it too
**Given** people have different likes and dislikes,
**When** eating food,
**Then** the site needs to have the ability to like or dislike the recipes and this information needs to be displayed clearly.
######  Results
*On the recipe card page there are thumbs up and thumbs down icons. When a recipe has been liked or disliked a number is displayed beside the icon*
![image](static/documentation_files/images/user_story_images/us2_likes.png)

*The icons also appear on buttons on the recipe detail page but the button can only be clicked if the visitor is logged in*

![image](static/documentation_files/images/user_story_images/us2_loggedin.png)

*If a logged in visitor clicks on the button a number will appear*

![image](static/documentation_files/images/user_story_images/us2_liked.png)

*If the logged in visitor clicks on the button a second time a flash message will appear*

![image](static/documentation_files/images/user_story_images/us2_sorry.png)
######  User Story 3:   Contact
**As a** visitor, 
**I want** to be able to contact the organisation
**So that** when I have a question or something is wrong
**When** using the site,
**Then** a confirmation email should be sent to the visitor.
######  Results
*There is a link in the footer of the website which allows a visitor to contact me*
![image](static/documentation_files/images/user_story_images/us3_contact_link.png)

*The visitor fills in this form and clicks the `send request` button*

![image](static/documentation_files/images/user_story_images/us3_contact.png)

*A Flash message appears letting the visitor know the email has been sent*

![image](static/documentation_files/images/user_story_images/us3_sent_confirm.png)

*The request is sent via email to my email address*

![image](static/documentation_files/images/user_story_images/us3_email_from_visitor.png)

*An automatic response is sent to the visitor on the email address they provided to confirm we have received their request*

![image](static/documentation_files/images/user_story_images/us3_email_response.png)

######  User Story 4:   Registration/Login
**As a** visitor, 
**I want** to know my account is secure to me
**So that** I am confident no one else will be able to access my recipes
**Given** that passwords need to be create,
**When** a new account is registered,
**Then** the new password needs to be confirmed and encrypted to reduce the risk of hacking and this password is then used to log into the account.
######  Results
The visitor needs to select the register menu option to be taken to the registration screen where they can create a username and password.
*The register option*

![image](static/documentation_files/images/user_story_images/us4_register_option.png)

*The visitor enters a unique username and a personal password twice to confirm the password is correct*

![image](static/documentation_files/images/user_story_images/us4_registration.png)

*On valid registration the visitor is take to their new profile page*

![image](static/documentation_files/images/user_story_images/us4_new_registration.png)

If the visitor makes any mistakes when registering they will recieve messages.
![image](static/documentation_files/images/username_already_exists.png)
![image](static/documentation_files/images/passwords_do_no_match.png)
*The password is encrypted before creating the user in MongoDB*
![image](static/documentation_files/images/user_story_images/us4_mongodb_user.png)

On subsequent visits the visitor can login via the login menu option.

*The login option*

![image](static/documentation_files/images/user_story_images/us4_login.png)

*The visitor is asked to enter their username and password*

![image](static/documentation_files/images/user_story_images/us4_login_page.png)

*On valid login the visitor is taken to their profile page*

![image](static/documentation_files/images/user_story_images/us4_profile_login.png)

If the visitor makes a mistake when trying to login they recieve a message.
![image](static/documentation_files/images/invalid_login.png)
######  User Story 5:   Upload Profile
**As a** visitor with an account, 
**I want** to be able to add an avitar or image of myself or change my password
**So that** I know I am on my own profile at a glance,
**Given** images are easier to register and password choices change,
**When** on the profile page
**Then** there needs to be an upload image and change password facility on the profile page.
######  Results
Upload an image

*On the profile page there is an upload image button*

![image](static/documentation_files/images/user_story_images/us5_newuser_profile.png)

*Clicking on the upload image button opens the upload profile image modal*

![image](static/documentation_files/images/user_story_images/us5_upload_modal.png)

*The visitor can then choose an image from their own file*

![image](static/documentation_files/images/user_story_images/us5_choose_image.png)

*The upload image modal will show the chosen image name*

![image](static/documentation_files/images/user_story_images/us5_upload_image.png)

*Clicking the upload button will attach the image to the user file in mongdb and display it on the profile page*

![image](static/documentation_files/images/user_story_images/us5_image_loaded.png)

Change Password

*Change password button*

![image](static/documentation_files/images/user_story_images/us5_change_password_button.png)

*Clicking on the change password button opens the change password page where the visitor can change their password*

![image](static/documentation_files/images/user_story_images/us5_change_password.png)

*When the password is successfully changed the visitor recieves a message*

![image](static/documentation_files/images/user_story_images/us5_change_success.png)

*The user file in mongodb is changed to reflect the new password*

![image](static/documentation_files/images/user_story_images/us5_newuser_mongodb.png)

If the visitor makes any mistakes when changing the password, they will receive some messages

![image](static/documentation_files/images/user_story_images/us5_old_password_error.png)
![image](static/documentation_files/images/user_story_images/us5_new_password_same.png)
![image](static/documentation_files/images/user_story_images/us5_passwords_different.png)
######  User Story 6:   Add Recipes/Categories
**As a** visitor, 
**I want** to be able to add my own recipes and categories
**So that** I can share them with family and friends
**Given** the visitor has registered, creating a profile,
**When** logged in,
**Then** the visitor can create, read, update and delete recipes from a single location as well as having the ability to create, read and update categories. The visitor cannot delete the categories unless they are logged in as admin and only then if there are no recipes associated with that category.
######  Results
The profile page is the main area and CRUD can be performed although, if a logged in visitor selects a recipe they have created via the home page or recipe cards there is the facility to change and delete that recipe.

*CRUD Recipe*

**Standard Visitor**
A standard visitor can only perform CRUD on their own recipes. They do not have access to perform CRUD on any other recipes

*Add a new recipe from the profile page by clicking on the `Add a new recipe` button*

![image](static/documentation_files/images/user_story_images/us6_new_recipe_btn.png) 

*This will open an empty recipe card where the visitor can create a new recipe including uploading an image of that recipe*

![image](static/documentation_files/images/user_story_images/us6_empty_recipe_card.png)

*The upload image button opens the upload new recipe image modal which works in the same way as the upload image modal for the profile page*

![image](static/documentation_files/images/user_story_images/us6_upload_new_image.png)

*Once an image has been chosen it is displayed on the page and a new recipe record exists in the recipes file in mongodb*

![image](static/documentation_files/images/user_story_images/us6_image_uploaded.png)
![image](static/documentation_files/images/user_story_images/us6_new_recipe_image_mongodb.png)

*The rest of the details can be added. It is possible to also create a recipe without an image. The image can be added later in the edit process*

![image](static/documentation_files/images/user_story_images/us6_new_recipe.png)

*The recipe is then displayed on the profile page along with a success message*

![image](static/documentation_files/images/user_story_images/us6_added_to_profile.png)

*The visitor can now maintain the recipe by using the `maintain recipe` button in the `My Recipes` table or by opening the recipe by clicking on its name. This will open the Change Recipe Page*

![image](static/documentation_files/images/user_story_images/us6_change_recipe.png)

*The upload image button allows the visitor to change the image*

![image](static/documentation_files/images/user_story_images/us6_new_image.png)

*Changing any other details will not change the recipe until the `Edit Recipe` button is clicked*

![image](static/documentation_files/images/user_story_images/us6_edit_button.png)

*With the exception of the image, the `Cancel` button will ignore any changes and take the visitor back to the profile page*

![image](static/documentation_files/images/user_story_images/us6_cancel_btn.png)

*The `Delete Recipe` button will take the visitor to a confirmation screen where they need to enter their password to be able to delete the recipe*

![image](static/documentation_files/images/user_story_images/us6_delete_btn.png)

*If they type the wrong password they will get a message to the recipe page*

![image](static/documentation_files/images/user_story_images/us6_recipe_deleted.png)

*If the recipe is deleted they will get a message and return to their profile page*

![image](static/documentation_files/images/user_story_images/us6_delete_recipe_confirm.png)

**Admin**

Admin can perform the same CRUD functions on all recipes, irrespective of ownership. Obviously, if there is a valid recipe `admin` should get permission from the recipe owner.
![image](static/documentation_files/images/user_story_images/us6_admin_recipes.png)

*CRUD Category*

**Standard Visitor**

A standard visitor can only perform CRU on their own categories. They cannot delete any categories because that category may be used by a recipe owned by someone else.
*To add a new category the visitor needs to click on the `Maintain Categories`button on their profile page.*

![image](static/documentation_files/images/user_story_images/us6_maintain_cats.png)
![image](static/documentation_files/images/user_story_images/us6_before_new_cat.png)
*Which will bring up the Manage Categories page where there is an `Add Category`button.*

![image](static/documentation_files/images/user_story_images/us6_add_cat.png)

*The `Add Category` page is very simple. The visitor simply types in the name of the category they wish to add*

![image](static/documentation_files/images/user_story_images/us6_add_cat_page.png)

*If the visitory tries to add a category that already exists, a flash message is displayed, the entry field is cleared and the category is not added.*

![image](static/documentation_files/images/user_story_images/us6_cat_exists.png)

*When a new category is successfully added, the visitor is taken back to the `Manage Categories`page and a flash message is displayed.*

![image](static/documentation_files/images/user_story_images/us6_new_cat_msg.png)
![image](static/documentation_files/images/user_story_images/us6_new_cat_after.png)

*The visitor can now change the category by clicking on the `change`button*

![image](static/documentation_files/images/user_story_images/us6_change_btn.png)

*The visitor can either click the `edit category` button or the `cancel` button depending on whether they want to keep the changes or not.*

![image](static/documentation_files/images/user_story_images/us6_change_cat.png)

*Once the change is accepted, the visitor is taken back to the `manage categories`page, a confirmation message is display and the changed category can be seen in the table.*

![image](static/documentation_files/images/user_story_images/us6_changed_cat.png)

**Admin**

`admin` can perform full CRUD functionality on categories. The website will not allow a category to be deleted if it is attached to a recipe. This can be checked on the recipe cards page using the search function.

*When admin selects `change`on the `Manage Categories` page, the `Update Category`page also has the delete function.*

![image](static/documentation_files/images/user_story_images/us6_admin_edit_cat.png)

*Clicking on the delete button will take `admin` to the delete confirmation screen where they will need to enter their password to be able to delete the category*

![image](static/documentation_files/images/user_story_images/us6_admin_delete.page.png)

*If they type the wrong password they will be taken back to the `Update Category`page and a flash messae will be displayed.*

![image](static/documentation_files/images/user_story_images/us6_admin_password_error.png)

*The system will not allow `admin` to delete a category that is currently attached to a recipe.*

![image](static/documentation_files/images/user_story_images/us6_fun_with_kids_delete.png)
![image](static/documentation_files/images/user_story_images/us6_cat_recipe.png)

*When a category is successfully deleted `admin` is taken back to the `Manage Category`page where a flash message is displayed and the category has been deleted.*
![image](static/documentation_files/images/user_story_images/us6_delete_cat_success.png)
