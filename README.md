# Mark Page #

This is a Chrome Extension used to mark a page with a certain state.

Currently it only allows the page to be marked with a state of read. On each page one visits, all the links on that page will be checked to see if they have already been marked as read. If they have been, then a small checkmark is placed next to the link. This makes it easy to see which pages you have not yet read.


## Install the extension ##

This project is still in very early age, so it's not yet available on the Chrome Web Store. However, you are welcome to download it from the repository, turn on "Developer Mode" in your Chrome browser, and try it out.

Please feel free to provide your feedback to improve this extension.

You can find the way to turn on the "Developer Mode" in the articles below:
- [Introduction To Chrome Extension Development](http://blog.iderzheng.com/introduction-to-chrome-extension-development/)
- [How can I set up Chrome for extension development?](https://developer.chrome.com/extensions/faq#faq-dev-01)


## Mark Page as Read ##

After you installed this extension, you can find a checkbox in your Chrome 
toolbar. Simply click on the checkbox to toggle the read state of the page
you are visiting.

![Mark Page as Read](docs/mark-page-as-read.png?raw=true "Mark Page as Read")

When you mark a page as read, the other pages in **the same domain** would 
display the indicators beside the links: "✓" for read page and "☞" for the page
anchor.

The read state is not visible on cross-domain pages, because the purpose of this
extension is to help you when you are studying online documents. You can
mark the pages as read and thus keep track of your progress.

The anchor mark is not visible until you mark a page in that domain as read,
which indicates that you have started to learn the documents.

## Option Menu ##

You can open the options page in Chrome "Manager Extensions" page

![Mark Page Options](docs/options-page.png?raw=true "Mark Page Options")


### View Read Pages ###

All marked pages are stored in the extension's local storage, you can visit
them in the options page, they are grouped by the domain:

![Read Pages](docs/read-pages.png?raw=true "Read Pages")

You can also download the read pages as a json file, in case Chrome clears
the extension data. 

### Manage Blackout Paths ###

The marked pages are domain based, however, there might be some paths you 
don't want to show the indicators, e.g: a forum, or a data diagram.

For those cases, you can add the sub paths in the "Blackout Paths" list:

![Blackout Paths](docs/blackout-paths.png?raw=true "Blackout Paths")

The path in the specified domain will not show the indicator if it starts
with any blackout path.    
We will support wildcard paths in the future for more complicated situations.


## Keybard Shortcut ##
`Ctrl + R`: Toggle the read state of the page you are visitin


## FAQ ##
- How do I remove a domain if I accidentally mark a page as read?     
Right now we don't have a option to delete a domain, you can add "/" to the
blackout paths to that domain, so no indicators show.

- Can I import that read page json file?    
We will support the file import to update the progress cross different 
computers in future.     
The json file will also contain the blackout paths.

- Can I use specify the blackout path as "contains"?    
To be simply, it currently checks "starts with" only, we can support wildcard
in future.

- I only need the checkmark, I don't want to see the anchor indicate, can I
turn it off?    
Not yet, but we will make the options pages more friendly.

