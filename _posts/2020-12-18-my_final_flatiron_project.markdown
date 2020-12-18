---
layout: post
title:      "My Final Flatiron Project"
date:       2020-12-18 06:24:11 +0000
permalink:  my_final_flatiron_project
---


My final Flatiron project 
I feel euphoric knowing I have come this far, and knowing that I finally completed my final project.
My project is based off of the NASA Open APIs. 
I have three components: astronomy pictures of the day, most viewed NASA projects, and pictures from the three Mars Rovers. 
This project was both the easiest and the hardest project I had to do. It was easy because I was doing it based on something I am very passionate about.
However, what really got me were two things. 
STATEEEE
and returning the proper objects from the fetch calls. 
Lets start with the easier of the two. Returning the objects from my fetch call. I knew I was going to have to create a new variable in my .then to save the information I wanted, however I did not know how nested the information was inside the actual API. With a lot of trial and error I was able to retrieve what I needed, but then I had issues with how it was rendering on my page, so once again I had it nested in too deeply and I had to go back in with console.log() and debugger to find out what my props were. My final code in both my actions file and my component file were as followed: 
```
export const getTechFour = () => {
   return (dispatch) => {
      return fetch(`https://api.nasa.gov/techport/api/projects/94151?api_key=bS7Kb4VfcpKaKmarzxrfcYlg8CJGzJ9m6CIajasm`)
       .then((resp) => resp.json())
       .then((result) =>{
       const techObj = {
           title: result.project.title,
           description: result.project.description,
           startDate: result.project.startDate,
           endDate: result.project.endDate,
           status: result.project.status
       }
       dispatch({ type: "FETCH_TECH4", payload: techObj })
       }
       );
   };
};
And 
const Project = (props) => {
  
   return (
           <div>
               <br></br>
               ★・・・・・・★・・・・・・★・・・・・・★・・・・・・★・・・・・・★・・・・・・★・・・・・・★
               <h2>{props.technology.title}</h2>
               <h3>{props.technology.startDate} - {props.technology.endDate}</h3>
               <h4>{props.technology.status}</h4>
               {props.technology.description}
           </div>
   )
}
```
 
So this brings me to my next and the biggest problem I struggled with. 
State. Since I was making multiple fetch calls that were all meant to render in one component I was facing numerous errors in trying to render them in the state all at once. So step by step. My first problem was in my reducer. I needed to create a variable set to initialstate that was assigned a hash with a key and a value of an empty array. Next I needed to push the state into that array and include the payload, so that it was all included. Okay take a breath. I then created my componentdidmount in my initial component including all of my different fetch calls. Then in my mapstatetoprops i made it that my state was composed of all of the different fetch calls as opposed to just one. And what was my divine savior was that I had to create a function that would then iterate through all of them and then go on to display my different projects in a separate component to keep things clean and in order. This can be confusing so the code goes as followed:
```
const initialState = {tech: []}
 
function technologyReducer(state= initialState, action ) {
   switch (action.type) {
       case "FETCH_TECHNOLOGY":
           return {...state, tech: [...state.tech, action.payload]};
 
           case "FETCH_TECH1":
           return {...state, tech: [...state.tech, action.payload]};
 
           case "FETCH_TECHN2":
           return {...state, tech: [...state.tech, action.payload]};
 
           case "FETCH_TECH3":
           return {...state, tech: [...state.tech, action.payload]};
 
           case "FETCH_TECH4":
           return {...state, tech: [...state.tech, action.payload]};
 
           default:
               return state;
   }
}
export default technologyReducer;
class Technology extends Component {
 
// fetch call
componentDidMount(){
   this.props.getTechnology();
   this.props.getTechOne();
   this.props.getTechTwo();
   this.props.getTechThree();
   this.props.getTechFour();
}
 
displayTech(){
   return this.props.tech.map(e => <Project technology={e} /> )
}
 
render(){
   return (
       <div>
           <h1>Most Viewed NASA Projects</h1>
           {this.displayTech()}
       </div>
   )
}
 
}
 
const mapStateToProps = state => ({ tech: state.technology.tech })
 
export default connect(mapStateToProps, { getTechnology, getTechOne, getTechTwo, getTechThree, getTechFour })(Technology);
```
This project came out better than I can ever hoped for; and as well as getting a really good understanding of React/Redux, I learned so many new tips and tricks for both React as well as CSS. I am so thankful and proud of how far I have come, and for how much I have grown. 

