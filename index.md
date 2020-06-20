# Alvaro Castillo ePortfolio

### Professional Self-Assesment 

   During the Computer Science Program at SNHU and the previous 5 years of studying different areas by my own I have obtained several skills and experiences that made me grow. My initial interest was related to video game development, so I was trying to learn from the different disciplines that make up that area and learning some general basic knowledge that serve as foundation for future skills.
  
   In the game development I started to learn how to program in different languages, which include C#, C++, and Java. I started to practice using the Unity Engine for it. Then I learned to use Blender and learned 3D modeling and sculpting together with graphic design and techniques to improve the artistic side of it. At the same time in the Computer Science Program I had learned the general concepts behind Agile Development, and more General Knowledge like Physics classes which I would latter use in the Unity Engine to simulate realistic physics and destruction, specially particle physics with the tools Unity provides.
 
   During the middle of the Computer Science Program I started to have more complex classes, I learned several practices related to Databases with SQL and NoSQL with MongoDB. During the same time I came upon GCP(Google Cloud Platform) since my stepfather who is a developer started studying it and certificated himself in it, I saw the huge power and versatility of Cloud computing and development and started studying to also certify myself in GCP. Because of this I learned some network security, big data, and analytics. Also, in the Computer Science program I learned a bit of Python when making REST APIs for MongoDB.
	
   Recently what I have interacted with a lot have been mobile and web development, I have been working making React JS components for web applications for a company and with Flutter and React Native for mobile applications as freelance. Also, the Computer Science program finale had a few android development classes where I got to practice more my Java skills and learn to use the native android language, but after using Flutter for a while and learning a lot of ways of making different things for mobile and web, I find the classes to be simple and outdated.
	
   The Artifact I plan to display ahead is one of the first Flutter apps I made, a simple administration app but in terms of ease of development compared to native Java the speed at which one can develop high quality apps with it is amazing, and the same codebase works in both iOS and Android with very little cost to performance which is a plus. In it I showcase this new technology and combine it with Firebase as backend, which is a NoSQL database similar to MongoDB that uses .json files for documents and also utilize the Authentication API of Firebase for managing access to the app and keep the information secure thanks to the Security Google provides.


### Artifact

#### Software Design and Engineering

   Using Flutter for the design of an app comes with some things that are different from the standard java or swift development, and the main one is that there are no xml files for the layout or any separation of UI and logic by file formats, this can be a problem for many developers to get used to, but once you get some practice in it brings significant speed when developing. In Flutter the language is dart which is a normal Object-Oriented Language very similar to Java or C#, in it also everything is a widget, and all widgets are added programmatically, which has a few advantages, the first one is that each widget is independent and modular, it means you can code one widget once and reuse it as many times you wish without any conflict compared to xml, another advantage is that since each widget can also hold logic within identifying them in a crowded UI is simpler. Another big advantage is in the Lifecycle, In Java one has to manage certain functionality using the onCreate method or onStart, in Flutter is managed with State and Stateless Widgets and the program manages the lifecycle without the developer getting involved. The Flutter SDK still is in its infancy, so it still lacks more specialized functionality but for a simple app like this one is significantly better than the standard way of making android apps.

#### Algorithm and Data Structures

   Data Structures in Flutter are not much different from Java, using a model class that holds the data of each object, the difference is that Flutter dart model classes don’t need getters or setters, the model class manages those using State. The algorithm behind this app is relatively simple because there is no complicated arithmetic operations, it follows this logic.
   
- The app starts with a Log In Screen, it has capability for Registering users but that feature is hidden as requested.
- App has forgot password button that sends to another screen asking for the email
 	1. 	If email exists it will send a link to the email with a password reset form
	2.	Else it will not send anything but still show the request sent message because of security
  
- App verifies users calling to a Firebase user list with an email and password.
 	1.	If user exists it moves to the Home Screen
  	2.	Else display error messages
  
-	In Home Screen app the program starts a Stream of data connected to the firebase backend
  	1.	If it connected to Firebase, it will start pulling stream data in form of firebase snapshots
    	2.	These snapshots are converted to Incident objects using the Incident model
    	3.	The objects are then Iterated by a List View Builder by their ID, as long as there Is an object with an ID it will be displayed in the List as a Clickable Card displaying the information of the object.
    
- Each List Item is clickable and redirects to a page that hold the whole Incident information.
- The Incident page holds the ID for the document that was clicked and the object model
- The Incident page has a Carousel Widget that works by giving it arrays of strings holding URLs to images.
  	1.	If there is an array object with the correct key holding several URL links, it will iterate on each string to display an        	interactable image.
  	2.	If there is an error with any link, or the value is null it will display an image that represents an error instead.
  	3.	If there is no correct key holding image strings it will display a single image similar to the one mentioned previously.
  
- The incident page uses the key value pairs in the object model to display the rest of the data in an easy to read way using    		expandable text fields.
  	1.	If any of the keys doesn’t exist of their values are null the app display a message to cover for it.
  
- The incident page has an erase button at the end, on click it will display a Bottom Sheet asking for confirmation since the 		action is irreversible
  	1.	If confirmed it will start a transaction request with Firebase to erase that document based on its ID, after the document is erased it will return to home screen and thanks to the stream it will be already updated without the erased documents in the list
  	2.	If clicked no, it will close the bottom sheet and return to the Incident page.
  
- Home page has a log off button, once clicked it will send back to log in and clear the firebase user information.

#### Database

In this app I utilize the power of the Google Cloud Firestore Database for storage, it is a NoSQL database similar to MongoDB, which uses key-value pairs. The schema of the database is relatively simple. This Image is a representation of a test object in it.
![Image](https://ibb.co/wWGVWnZ)
	


You can use the [editor on GitHub](https://github.com/dailandemon/dailandemon.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Alvaro Castillo EPortfolio
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/dailandemon/dailandemon.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
