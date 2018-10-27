Issues found in Current Design :

1) Chrome Driver version 2.33 was used against the update 2.42
2) "ToTag" webelement locator was wrong
3) Date picker XPATH was for old date 
4) For HotelBooking testcase , PageFactory initialization of elements was missing 
5) Missing code to click on the destination auto popup in HotelBooking
6) Assertion for HotelBooking was missing
7) Switching to frame was missing in SignIn Test
8) All the tests are written in pageclass itself

New Design Implemented and Issues fixed :

1) Updated chrome driver to 2.42
2) Updated all wrong locators
3) Separated all page classes in a new package and driver class
4) Global driver object is initialized and been passed as a constructor param during object creation of page classes .
5) Created a new FrameWorkUtilities.java class which was static isElementDisplayed , setDriverPath , waitFor methods 
6) All drivers and pageclasses and drivers extend FrameworkUtilities.java so that they can access the static methods defined in previous step
7) Parameterized shouldBeAbleToSearchForHotels , testThatResultsAppearForAOneWayJourney to take user defined values