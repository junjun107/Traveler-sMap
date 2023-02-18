## Full Stack Travel Journal

A fullstack travel map app allows users to track their travel destinations around the world. Users can view destinations on an interactive map, save their favorite places, and create custom itineraries. 


The backend of a fullstack travel map app built with Node.js, Express, and MongoDB. 

The frontend of a fullstack travel map app built with React, React Map GL, and Material-UI provides a user-friendly and visually appealing interface for searching and exploring destinations.


#### Setup development environment use Create React App

```
npx create-react-app my-app
cd my-app
npm start
```

#### Use React Map GL

React Map GL is a React library that provides an easy-to-use API for integrating maps into a React application. It is built on top of the popular Mapbox GL library and allows for the display of maps, markers, and other map features.

```
npm install react-map-gl mapbox-gl
```

#### React fetching data from Node.js with useEffect

```
const getEntries = async () => {
    const logEntries = await listLogEntries();
    setLongEntries(logEntries);
  };

  useEffect(() => {
    getEntries();
  }, []);
```

### Display logs with React Map GL Maker and Popup on map dynamically

```
 {logEntries.map((entry) => (
        <React.Fragment>
          <Marker> {/* ... /} </Marker>
            <Popup>{/* ... /}</Popup>
        </React.Fragment>
      ))}
```

### Implement a forum when double click on map

### Issues:

Cors Origin Error
Cores Origin url in the backend doesn't match the frontend url localhost:3000

production build error "x is not defined" 
Map from mapbox api didn't show up during production. Reason to that is because the JavaScript bundle is incompatible with some Babel transforms because of the way it shares code between the main thread and Web Worker. 
To fix that, I explicitly disable transpiling of the Mapbox GL JS bundle.
