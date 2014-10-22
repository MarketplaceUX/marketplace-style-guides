# The Feed: Adaptive Firefox Marketplace

## Contents
1. Change Log
2. Project Overview
3. User Stories
	3.1. Relevant User Stories from PRD addressed by Design Stories
	3.2. Design Stories
		3.2.1. Design_Story_01 -- Marketplace Navigation Across Platforms 
		3.2.2. Design_Story_02 -- The Feed View Across Platforms
		3.2.3. Design_Story_03 -- New Apps View Across Platforms
		3.2.4. Design_Story_04 -- Popular Apps View Across Platforms
		3.2.5. Design_Story_05 -- Categories View Across Platforms
		3.2.6. Design_Story_06 -- Community View Across Platforms
		3.2.7. Design_Story_07 -- Profile View Across Platforms
		3.2.8. Design_Story_08 -- Apps & Collections View Across Platforms
		3.2.9. Design_Story_09 -- App Details View Across Platforms
		3.2.10. Design_Story_10 -- Search Results View Across Platforms
		3.2.11. Design_Story_11 -- HTTP Error States Views Across Platforms
4. Appendix A: Frameless Grid
5. Appendix B: Native Files

## Change Log
1. 22 March 2014: Initial version drafted by Tony Santos(asantos@mozilla.com)
## Project Overview
### Overall Project
This design project is part of the larger Desktop Marketplace project, as defined in the PRD Desktop Marketplace v2 PRD(https://docs.google.com/document/d/1o5mw54p4GAnE8xUUbG1hPJSezbevFMtQ_ZG5eMRpXQE). This project concerns itself only with the display of the Marketplace Feed across platforms. Additional features are defined in other design documents as noted in the PRD.
### This design project's goals
The goals of this project are to define the way the Firefox Marketplace displays itself across platforms. This will create a more tailored experience for consumers via a set of user interfaces that match their expectations on each platform. For the sake of simplicity we have started with three initial platforms: mobile, tablet and desktop. Additional adaptive states may be required in the future and they will be detailed in updated versions of this document.

## User Stories
### Relevant User Stories from PRD addressed by Design Stories
#### User_Story_01 
As a Desktop Consumer, I would like to be able to view desktop-only apps or all apps (mobile, desktop, etc.) and switch between these views so that if I am interested in only apps that will work on my desktop, I will just see those, but if I am interested in browsing all apps, I should be able to see even apps that won’t work on my desktop. This filtering should apply to all apps that are viewed.
#### User_Story_02
As a Desktop User I would like to browse apps by category. 
#### User_Story_03
As a Desktop User I would like to discover apps that are most popular on the Marketplace.
#### User_Story_04
As a Desktop User I would like to discover apps that were recently added to the Marketplace.
#### User_Story_05
As a Desktop User I would like to view a list of my collections and apps within each collection
#### User_Story_06
As a Desktop User I would like to be able to add, delete, modify my display name is text so that I can share this information with others.
#### User_Story_07
As a Desktop User I would like to be able to add, delete, modify biography information as text so that I can share this information with others (up to 500 characters?)
#### User_Story_08
As a Desktop User I would like to be able to add, delete, modify  my location information  as text so that I can share this information with others.
#### User_Story_09
As a Desktop User I would like to be able to opt-in/out of notifications and email so that I am able to be notified of marketplace information.
#### User_Story_10
As a Desktop User I would like to see Community Collections and apps within those collections only if there are at least 3 (?) apps that I am able to view given the filters that I have.

### Design Stories
#### Design_Story_01 -- Marketplace Navigation Across Platforms
##### Addresses: none? (user story needed?)
##### Solution:
The navigation of the Marketplace contains the main sections of the Marketplace app: Home, New, Popular, Categories, Community (Community is a v2 Feature), My Account. The Categories menu contains a sub-menu with entries for each category in the Marketplace. The My Account menu is only visible when a user is logged in. It contains the sub-menu with entries: Profile, Apps & Collections. 
###### On 4 column (mobile) layout:
The menu is a scrollable horizontal menu with magnetic links (i.e. the selection snaps to the next item in the list as the user scrolls.) under the app's header. The current location of the user in the hierarchy is indicated by the underline that is a fixed point on the left side of the menu. The settings submenu is available by tapping the settings button on the left side of the menu. Tapping the Marketplace button on the right side of the settings menu brings the user back to the main menu. Example of the menu behavior at (http://people.mozilla.org/~asantos/feedPrototypes/navPrototypeMarch2014/mobile_feed_nav_changes.html) 
[images from prototype]
###### On 8 column (tablet) layout:
The menu is a fixed horizontal list under the app's header. The current location of the user in the hierarchy is indicated by the underline that moves from menu item to menu item.
??The menu labels are wrong on all the images. Need to be updated??
[images from wireframes]
###### On 12+ column (desktop) layout:
The menu is a fixed horizontal list under the app's header. The current location of the user in the hierarchy is indicated by the underline that moves from menu item to menu item.
??The menu labels are wrong on all the images. Need to be updated. Are we using breadcrumbs or not??
[images from wireframes]
###### Visual guidelines:
[visual design stuff here]

#### Design_Story_02 -- The Feed View Across Platforms
##### Addresses: none? (user story needed)
##### Solution:
A user is presented with The Feed, a highly curated, editorialized stream of content as the homepage on every platform. As the screen space grows from 4 columns (mobile), to 8 columns (tablet), and to 12+ columns (desktop), the content of the feed stays consistent, but it's display changes significantly.
###### on 4 column (mobile) layout:
The feed displays as a long vertical scrolling list, similar to the news feed in a social network. If the user is on a partner cell network, the top unit in the display is that partner's Operator Shelf unit. After that, the feed is a dynamic list of apps content created by the Marketplace Editorial Staff using the available feed unit types, all 4 columns wide. 
###### on 8 column (tablet) layout:
###### on 12+ column (desktop) layout:
###### Visual guidelines:
??We seem to be missing this page completely for tablet and desktop??

#### Design_Story_03 -- New Apps View Across Platforms 
##### Addresses: User_Story_01, User_Story_04
##### Solution:
When the user selects the "New" item from the main navigation the Marketplace returns the 100 newest apps in the catalog, sorted newest to oldest. This view includes a section titled "New this week" that highlights the three most popular apps in the 100 newest. 

??We have 3 on desktop, 2 on tablet, and 1 on mobile. This feels odd. Can we keep this the most popular app in this set and then show more info about it in a larger unit on the larger screens?(e.g. ratings and reviews on tablet and desktop. We know these are important to users, surfacing them feels like a better way to use the space. We're missing filters on this page.??
###### on 4 column (mobile) layout:
The New Apps view starts with the New This Week unit. It then alternates between a 3x1 icon grid and a detailed icon unit, showing two of each before the rest of the apps are displayed in a 3x31 grid. 
[images from wireframes]
###### on 8 column (tablet) layout:
The New Apps view starts with two new this week units, each 4 columns wide, and is followed up by a section showing 6x2 apps in icon view.
??Why are we wrapping these in boxes? Is this an artifact from screen scraping to get assets or was this the intention. The icons could float in a grid view without any of the boxes.Do these icons scroll and if so is that indicated anywhere in the Ui, like it is in the desktop??
###### on 12+ column (desktop) layout
The New Apps view starts with three New This Week units, each 4 columns wide, and is followed up by a horizontally scrolling section showing 9x3 apps in icon view.
??This horizontally scrolling unit behavior is inconsistent with other sections of the app??
###### Visual guidelines:

#### Design_Story_04 -- Popular Apps View Across Platforms 
##### Addresses: User_Story_01, User_Story_03
##### Solution:
When the user selects the "Popular" item from the main navigation the Marketplace returns the 100 most popular apps in the catalog, sorted most to least popular, where popular is defined using our current algorithm for popularity.

??Why are we removing "Popular this Week" on the tablet and the desktop? This seems like a totally different list when we get to the tablet and desktop. We're missing filters on this page??
###### on 4 column (mobile) layout:
This view includes a section titled "Popular this week" that highlights the three most popular apps in the last week, the rest of the view is an ordered list of all-time popularity.

###### on 8 column (tablet) layout:
This view includes a section titled "Popular collections" that highlights two popular user collections. The rest of the view is a 2x3 grid of app details units sorted by popularity.
??There needs to be some order to these apps explicitly stated.Do these icons scroll and if so is that indicated anywhere in the Ui, like it is in the desktop??
###### on 12+ column (desktop) layout:
This view includes a section titled "Popular collections" that highlights three popular user collections. The rest of the view is a horizontally scrolling 3x3 grid of app details units sorted by popularity.
??There needs to be some order to these apps explicitly stated. This horizontally scrolling unit behavior is inconsistent with other sections of the app??

###### Visual guidelines:

#### Design_Story_05 -- Categories View Across Platforms 
##### Addresses: User_Story_02
##### Solution:
###### on 4 column (mobile) layout:
When the user selects the Categories item on the main navigation, the Marketplace returns a grid of category icons. Selecting one of these takes the user to a list view of the apps in that category sorted by popularity. Tapping the categories menu item again brings the categories grid back up from the bottom. 
###### on 8 column (tablet) layout:
###### on 12+ column (desktop) layout:
###### Visual guidelines:
??We seem to be missing this page completely??

#### Design_Story_06 -- Community View Across Platforms 
##### Addresses: User_Story_10
##### Solution: 
!! Note, this is a v2 story !!
When the user selects "Community" item from the main navigation, the Marketplace returns a list a community created collections sorted by popularity.
###### on 4 column (mobile) layout:
The list of collections mirrors the feed's long vertical scrolling format, and each collection is shown using it's mobile feed unit display type. 
###### on 8 column (tablet) layout:
The list of collections is split into two sections, Popular collections which shows as a 2x2 grid of collections, using the mobile feed unit display type. The "see more" link next to the section title allows the user to "see more" in a screen that looks like....
??This "see more" behavior is inconsistent. If this is the behavior we're going with, what does the "see more" view look like? Why do we feel like it's a good idea to segment the information this way??
###### on 12+ column (desktop) layout:
The list of collections is split into three sections: Popular Collections, New Collections, and Your Collections. Popular collections is a five unit grid with three collections displayed on the top row using their mobile feed unit display type, and two units on the bottom row using a larger 6 column wide display type. New collections is a single row consisting of four collections, all shown using the mobile feed unit display type. Your collections is a single row consisting of four collections, all shown using the mobile feed unit display type. This section also includes a "Create a new collection" button.
 ??This "see more" behavior is inconsistent. If this is the behavior we're going with, what does the "see more" view look like? Why do we feel like it's a good idea to segment the information this way?? 
###### Visual guidelines:

#### Design_Story_07 -- Profile View Across Platforms 
##### Addresses: User_Story_07, User_Story_08, User_Story_09
##### Solution:
 When the user selects "My Account" from the main navigation or the "Profile" submenu item, the Marketplace displays the user's profile page. This page is always in editing more, with all values shown as input elements.
###### on 4 column (mobile) layout:
[insert images from wireframes]
###### on 8 column (tablet) layout:
[insert images from wireframes]
###### on 12+ column (desktop) layout:
[insert images from wireframes]
###### Visual guidelines:

#### Design_Story_08 -- Apps & Collections View Across Platforms 
##### Addresses: User_Story_05
##### Solution:
!!Note: This is a v2 story !!
###### on 4 column (mobile) layout:
When the user selects the Apps & Collections menu item the Marketplace returns a page with a three option segmented control at the top for: Collections, Wishlist and My Apps. The collections option is the default option and it shows a page with a list of all the user's collections (if any) sorted by newest. At the top of the list is a button labeled "Create a new collection" the kicks off the Community Collection builder. The Wishlist view is a list sorted by newest of apps the user has saved to her wishlist (if any.) The My Apps view is a list sorted by newest of apps the user has installed(if any.)   
??What do these lists do when they're empty??
###### on 8 column (tablet) layout:
When the user selects the Apps & Collections item from the My Account menu the Marketplace returns a page containing three sections: Collections, Wishlist, and My Apps. The Collections section is an 8 column wide, 2x2 horizontally scrolling grid showing collections with their mobile feed unit display type. There is a "Create new collection" button at the top of this section that kicks off the Community Collection builder. The Wishlist section is a 4 column wide list of applications the  user has added to her wishlist (if any). The My Apps section is a 4 column wide list of apps the user has installed (if any.)
??What do these lists do when they're empty. The horizontal scroll is inconsistent with other grid views in the spec. Which are we doing??
###### on 12+ column (desktop) layout:
When the user selects the Apps & Collections item from the My Account menu the Marketplace returns a page containing three sections: Collections, Wishlist, and My Apps. The Collections section is an 12 column wide, 2x2 grid showing collections with their mobile feed unit display type with edit and make public controls to the right of each collection. There is a "Create new collection" button at the top of this section that kicks off the Community Collection builder. The Wishlist section is a 4 column wide list of applications the  user has added to her wishlist (if any). The My Apps section is a 8 column wide, side-by-side list of apps the user has installed (if any.)
??What do these lists do when they're empty Where did the horizontal scroll elements go from the tablet view, what happens if there are more than 4 collections here? Why are we only surfacing edit and make public controls for collections in the desktop view? ??
###### Visual guidelines:

#### Design_Story_09 -- App Details View Across Platforms 
##### Addresses: none? (user story needed?)
##### Solution:
When a user selects an individual app from any list or feed unit the Marketplace shows the app's app details page. 
??We're missing the Write a Review, Report App Issue, And Report Abuse forms as well as the Privacy Policy view for all platforms.??
###### on 4 column (mobile) layout:
The main navigation is replaces with a back button and search bar at the top of the page. Screen shots are displayed in a horizontally scrolling list view. Tapping any of the "more" links will expand the section vertically to it's full height, pushing any content below it down. Clicking the write a review button takes the user to the write a review form. Clicking the report App issue button takes the user to the report an app issue form. Clicking the Privacy Policy button opens the app's privacy policy. Clicking on the Report abuse button opens the report abuse form. The Homepage and Support Email buttons are hyperlinks to the URL and Email address provided by the developer when she submitted the app. 
###### on 8 column (tablet) layout:
The main navigation stays intact. Tapping any of the "more" links will expand the section vertically to it's full height, pushing any content below it down. Clicking the write a review button takes the user to the write a review form. Clicking the report App issue button takes the user to the report an app issue form. Clicking the Privacy Policy button opens the app's privacy policy. Clicking on the Report abuse button opens the report abuse form. The Homepage and Support Email buttons are hyperlinks to the URL and Email address provided by the developer when she submitted the app.
??Why did some of the buttons move into a new column, but not all??
###### on 12+ column (desktop) layout:
The main navigation stays intact. Tapping any of the "more" links will expand the section vertically to it's full height, pushing any content below it down. The reviews section expands to a side-by-side layout with each review displayed at five columns wide. Clicking the write a review button takes the user to the write a review form. Clicking the report App issue button takes the user to the report an app issue form. Clicking the Privacy Policy button opens the app's privacy policy. Clicking on the Report abuse button opens the report abuse form. The Homepage and Support Email buttons are hyperlinks to the URL and Email address provided by the developer when she submitted the app.
??Why did some of the buttons move into a new column, but not all Why are there more links in this view???

###### Visual guidelines:

#### Design_Story_10 -- Search Results View Across Platforms
##### Addresses: User_Story_01
##### Solution:
When the user uses the marketplace search field, the Marketplace serves up the results as a list of up to 25 apps at a time.

??There are no platform filters in any view. What happens when the result is "no results found"??
###### on 4 column (mobile) layout:
The main navigation is replaced by the full search field with the search term preserved and a back button. The apps are listed  in their condensed results view spanning all 4 available grid columns. Selecting the grid icon from the view filter at the top displays the search results in their expanded results view. 
??The expanded view is missing for the phone layout??
###### on 8 column (tablet) layout:
The main navigation remains intact. The apps are listed in their condensed results view spanning all 8 available grid columns. Selecting the grid icon from the view filter at the top displays the search results in their expanded results view. 
###### on 12+ column (desktop) layout:
The main navigation remains intact. The apps are listed in their condensed results view spanning the first 8 grid columns. Related community created collections (if any) are displayed to the right, each collection is displayed in it's mobile feed unit display type. Selecting the grid icon from the view filter at the top displays the search results in their expanded results view.
??Are we doing breadcrumbs or not? This is the only page they show up on.??
###### Visual guidelines:

#### Design_Story_11 -- HTTP Error States Views Across Platforms
##### Addresses: 
##### Solution:
###### on 4 column (mobile) layout:
###### on 8 column (tablet) layout:
###### on 12+ column (desktop) layout:
###### Visual guidelines:

		
		
		
		
		
		
		