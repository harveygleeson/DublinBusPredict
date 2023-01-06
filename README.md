# Dublin Bus Travel Planner App

Dublin Bus Travel Planner App developed using Django and React. The app allows users to plan a journey between two locations using Google Maps API, which is set to plan journeys only via foot or Dublin Bus. Users can also view all available current Dublin Bus routes, via the route information button. The web app is adapted to fit all screen sizes, and has an alternative layout for phone/tablet. User current location, stops within 500m, and current weather are all accessible from the main screen. Journey times are predicted using a random forest model for each bus route, added to walking times calculated by Google Maps API. 

## Backend
Django connects to an Amazon RDS service, which holds current bus route information such as bus number, bus stop location, journey direction, and the coordinates of each bus route. These are served to the frontend via REST API calls, and displayed on the app through state changes.

## Frontend
The frontend is built with ReactJS. The `components` folder holds all UI components, such as `map`, `navbar`, and `weather` features. All features are accessed via modals which hover over the map, which are stored in the `Modals` folder. This folder contains files for `JourneyPlannerModal`, `RoutesModal`, and `ChooseRouteModal`, as well as an overall `Modal` file which is responsible for holding the contents of what is to be displayed (similar to a card).

Testing is implemented with React Testing Library for each of the components, to ensure they mount correctly, and that correct data is passed between them via props and held in component state.

## Screenshots

### Home screen for web app upon opening on laptop:

<img src="assets/Screenshot 2023-01-06 at 13.49.59.png" width="600" alt="webapp">

### Home screen for web app upon opening on mobile/tablet:

<img src="assets/Screenshot 2023-01-06 at 14.13.44.png" width="300" alt="phoneapp">

### Home screen for web app with journey planner display:
<img src="assets/Screenshot 2023-01-06 at 13.50.36.png" width="300" alt="phoneapp with journey planner">

### Home screen for web app with future journey planner display:
<img src="assets/Screenshot 2023-01-06 at 13.50.55.png" width="300" alt="phoneapp with future journey planner">
