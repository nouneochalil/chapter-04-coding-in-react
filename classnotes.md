class -4

Creating food ordering app - Food Villa in this session
Create low level design -> Create app layout

header
    logo (Title)
    nav items (right side)
    cart
body
    search bar
    restaurantList
      restaurantCard
        image
        Name
        Rating
        Cuisine
footer
   links
   copyright

-> Create HeaderComponent -> Add TitleComponent -> it has logo img and a tag for the image. -> div nav-items (ul and li )

-> Create Body and Footer Component

-> Create AppLayout -> put header, body and footer within <></>

JSX has only one parent ->use React.Fragment -> its like empty tag -> <> </>

but if you want to give attrbutes, style -> div tag

style = { border : red 1px soild} ; -> not possible -> wrap inside () inside jsx

restaurantcard  -> hardcoded card(ie,image and data wl b always same) ->it should be dynamic ->for this we can use js inside html ->
//Build the static version of restaurant view and restaurant card with hardcoded values. Then, pass data model to it.

In our case, we are using mock data for now (`swiggy mock data`)which contains information about a list of restaurants. First understand the data model, where can we find the required objects like restaurant name, cuisines, avg rating, delivery time and image in the data hierarchy.

Once data model is ready, use the data to populate the restaurant view by looping (use array map function ie for each restaurant in the array, tranform the restaurant data into restaurant card by writing jsx). Pass restaurant data as Props to the RestaurantCard//
`


`Config - driven UI : Different UI layout for different users - Backend driven config`

Optional chaining ?

Props (properties) passed in Component are similar to the arguments passed in a js function call and received by the function definition as parameters.

const Component = (props)=>{()} :: func(arguments) : const func = (parameters) => {}

Virtual DOM -> representation/copy of DOM with us

Purpose : React Reconciliation -> React uses diff Algorithm to diff one tree (actually dom) from another which determines what needs to be updated and only re-renders the diff

re-render everything if key is not mentioned

react fiber

never use index as key

