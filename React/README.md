Q1====Suppoose you want to create a form and when someone inputs the stuff ,you want to store it in state using useState

const [name,setName]=useState("");

<form>
  <input type="text" value={name} OnChange={(e)=>setName(e.target.value)}><input/>
<form/>

Q2=====Now state is Updated and user clicks the submit button on the form
how to handle this submit button thing

const [name,setName]=useState("");

<form  OnSubmit={handleSubmit}>
  <input type="text" value={name} OnChange={(e)=>setName(e.target.value)}><input/>
<form/>

function handleSubmit(e)
{
e.prevent default();
//this will ensure that page does not reload when sumbit is clicked because it is a single page application

if(!name) return;
//this statement will ensure that new object is not created when there is no name

const newFriend=
{
username
}

setName('');
//this will change the value of state back to empty

}

//this new object will be formed when someone clicks the submit button and value of name will get added to this object.
//Doubt=what is e here and what is the use of e here == e is the event which will happen when user clicks the submit button . when somenone clicks the submit button , value of sutff stored in states will automatically be sent to handleSubmit Fucntion via e.

Q3====Now we have made a object but still is not displayed on the screen so we need to add this object to a array so that it can be displayed

initialnames=[{username:amaan}{username:mohd}] //this is the array which contains some initial names

const[allnames,setNames]=useState(initialnames);
//allnames array will contain all the names and we will add new names to the allnames array

function handleAddNames(name){
setNames(allnames => [...allnames,name]);
}
//creating the function is not enough ,pass the function down to place where we are adding new friend that is the form

<FormAddFriend onAddNames={handleAddNames}/>
//passed it down to the form but now recieve it the form but cant show the whole function here so only clipping the small snippet

function FormAddFriend({onAddNames}) {

//now you are ready to use the "onAddNames" function in this fucntion .call the fucntion now.

Q4====The concept of lifting up state and passing them down.we will take the same exaple but diifrent scenario

suppose there is a state named
const[allnames,setNames]=useState(initialnames);
you want to use this state in your application but in which function do you use it

<app/>
<nameList/>
<form-add-names>

so in this case we need that in both the fucntions  
<nameList/>
<form-add-names>
so we need to place the state somewhere it can be accessible to every fuction so we make the state in <app/>

done but what if <nameList/> wants to use the state variable "allnames" .
if you use it there , it will show error "allnames is not defined"
for this to work we need to pass the "allnames" down to the functions adn ask them to recieve it.

how to pass them down
<nameList allnames={allnames}/>

how do we recieve them in the fucntion "nameList"
function namelist({allnames}){
}

Q5====explaing the onclick and how the button works in the bill-split application
