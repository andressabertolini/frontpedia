## Page navigation with routes

[Create an app](https://github.com/andressabertolini/frontpedia/blob/main/ReactJS/Create%20an%20app.md)

After creating the app, access the directory
```
cd app-name
```

Install the router package
```
npm install react-router-dom
```

> [!NOTE]
> react-router is a library for managing routes in React applications. It allows you to define and navigate between different pages or sections of your app, and react-router-dom is a browser-specific version of this library. DOM stands for 'Document Object Model' (the HTML elements of a web application in simple words).

First, let's create the components. We'll create the navigation component. Inside the "src" folder, create a folder called "layouts"

Inside the layouts folder, create a file called **Navigation.js**

The structure of this component is as follows:

```
import { NavLink } from "react-router-dom";

const Navigation = () => {
    return <div>
        <NavLink exact to="/">Home</NavLink>
        <NavLink exact to="/about">About</NavLink>
        <NavLink exact to="/contact">Contact</NavLink>
    </div>;
};

export default Navigation;
```

> [!NOTE]
> NavLink is imported in {} because it's a named export

> [!NOTE]
> Exact ensures that the "Home" link will only be activated when the URL is exactly "https://yoursite.com/", and not on URLs that contain the path / followed by other subroutes (such as /about or /contact). Without exact, the NavLink to "Home" would be activated on any URL that starts with /, which would cause the link to not activate correctly on internal pages.

The other components will be the pages, create the “pages” folder inside the “src” folder. Create the files “Home.js”, “About.js” and “Contact.js” inside this folder

Home.js
```
const Home = () => {
    return <div>
        <h1>Home</h1>
    </div>;
};

export default Home;
```

About.js
```
const About = () => {
    return <div>
        <h1>About</h1>
    </div>;
};

export default About;
```

Contact.js
```
const Contact = () => {
    return <div>
        <h1>Contact</h1>
    </div>;
};

export default Contact;
```

Now that we've created everything we need, it's time to put it all together. In the "src" folder, open the App.js file and import the react-router-dom components:

```
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
```

> [!NOTE]
> Here, we are importing three main components from react-router-dom: BrowserRouter, Routes, and Route. In the part, "BrowserRouter as Router", we are simply creating an alias (Router) for the BrowserRouter.

We will need to import all the components we created, we can add comments /* layout */ and /* pages */ to better organize the project:

```
/* Layout */
import Navigation from './layouts/Navigation';
/* Pages */
import Home from './pages/Home';
import About from './pages/About';
import Contact from './pages/Contact';
```

Finally, we will create the routes for our menu with the <Navigation /> component inside the App() function. (You can delete the default content)
```
<Router>
  <Navigation />

  <Routes>
      <Route path="/" element={<Home />} />
      <Route path="/about" element={<About />} />
      <Route path="/contact" element={<Contact />} />
  </Routes>
</Router>
```

And our App.js file will look like this:
```
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
/* Layout */
import Navigation from './layouts/Navigation';
/* Pages */
import Home from './pages/Home';
import About from './pages/About';
import Contact from './pages/Contact';

function App() {
  return (
    <div>
      <Router>
        <Navigation />

        <Routes>
            <Route path="/" element={<Home />} />
            <Route path="/about" element={<About />} />
            <Route path="/contact" element={<Contact />} />
        </Routes>
      </Router>
    </div>
  );
}

export default App;
```

Now just run the project and we're done
```
npm start
```

