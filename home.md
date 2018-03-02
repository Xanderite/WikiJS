<!-- TITLE: Ad Inserter - User Guide -->
<!-- SUBTITLE: How to use and set up the Ad Inserter for the demo site -->

# Access Inserter Settings
1. Login to Wordpress (go to the site and click the log in link in the side bar)
2. Use the sidebar navigation to go to `settings` -> `Ad Inserter`

# Overview of Settings
![Ad Inserter Annotation](/uploads/ad-inserter-annotation.png "Ad Inserter Annotation")

1. **Block Selection**
There are 16 blocks, each block represents some html that will be injected into some page.
2. **HTML editor**
This allows you to edit what HTML will be used for the selected block, it can be none.
3. **Save Button**
Saves the current settings, and applies them to the site
4. **Automatic Insertion Settings**
When enabled, the block will be automatically inserted onto the site, in various positions such as: “Before Post” or “After Excerpt”. There is also a visual reference, when the show button is clicked.
Finally you can set how the html is aligned where it is injected.
*(**note:** some insertions positions may not work due to limitations of the theme, if you can’t see an ad you expect, check to see if its the selected insertion position that is the issue)*
5. **Target Pages**
Allows block level targeting of pages, based on post, or page.
6. **Additional Options**
	* Lists
		* Allows the blacklisting or whitelisting of the block based on various parameters, i.e. tag, category, url
	* Manual
		* Provides the option of manually inserting a Block using code, perhaps in a post or static page.
	* Devices
		* Restrict usage of block to device type, i.e. desktop, tablet and phone.
	* Misc
		* An assortment of other filters.

# Setting up an Embed Script
First you need to grab an embed script.
1. Login to the console, navigate to -> `My Publications`.
2. Select a publication and click on it.
3. Select a Behaviour and click on it.
4. Click on the embed code, and it will be copied to your clip board.

Now to use it with the Ad Inserter:
(only one embed script should be used a time, so make sure there isn’t one used in any of the other blocks)
1. Select a block to use.
2. Paste in the script from the above steps into the HTML Editor.
3. Select Footer for the Automatic Insertion.
4. Make sure the targeting is setup to target everything.

## Adding Embed Slots
Next you will need to grab some Slot tags, these determine which ads will be shown where.
1. Using the same login used to get the embed script, navigate to -> `Ad Slots` .
2. Select and click on an ad slot.
3. Click on the HTML EMBED TAG code, and it will be copied to the clipboard.

Now in the Ad Inserter settings
1. Select an unused block.
2. Paste in the HTML EMBED TAG from the above steps into the HTML editor.
3. Now select where the slot should be inserted using Automatic Insertion, and how it should be aligned.
(or optionally use manual insertion to insert in a specific page or post, described above).
4. Finally determine what filters should be placed on showing this ad slot. e.g. only show on pages with the tag “Football”.

# Setting up an Ad Tag
Once again, first find the Ad Tag in the console.
1. Login to the console, navigate to -> `Ad Tags`
2. Select and click on an Ad Tag.
3. Click view Ad Tag.
4. Click on the ad tag to copy it to the clipboard.

Now in the ad Inserter Settings:
1. Select an unused block.
2. Paste in the Ad Tag from the above steps into the HTML editor.
3. Now select where the ad tag should be inserted using Automatic Insertion, and how it should be aligned.
(or optionally use manual insertion to insert in a specific page or post, described above).
4. Finally determine what filters should be placed on showing this ad tag. e.g. only show on pages with the tag “Football”.

# Setting up the correct Ad Tag
Some Ad Tags in the console are configured to be shown in a 3rd party ad tag. An ad tag configured in this way will not be inserted correctly via the ad Inserter, it will be position at the top right of the page it is inserted on. Using the 3rd part ad tag will work in this case. 

To clarify:
* If an Ad Tag is to be used by a 3rd party network such as DoubleClick_DFP the console provided ad tag will not be aligned correctly when used directly.
* If the DoubleClick_DFP ad tag, that uses the console ad tag, is used then it should display properly.

## Using an Ad Tag with Embed Scripts
Using an Ad Tag does not require an embed script to be setup, and setting up an embed script should not interfere with an Ad Tag.

