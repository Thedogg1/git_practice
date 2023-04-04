let story = 'Last weekend, I took literally the most beautifull bike ride of my life. The route is called "The 9W to Nyack" and it stretches all the way from Riverside Park in Manhattan to South Nyack, New Jersey. It\'s really an adventure from beginning to end! It is a 48 mile loop and it literally took me an entire day. I stopped at Riverbank State Park to take some artsy photos. It was a short stop, though, because I had a freaking long way to go. After a quick photo op at the very popular Little Red Lighthouse I began my trek across the George Washington Bridge into New Jersey. The GW is a breathtaking 4,760 feet long! I was already very tired by the time I got to the other side. An hour later, I reached Greenbrook Nature Sanctuary, an extremely beautifull park along the coast of the Hudson. Something that was very surprising to me was that near the end of the route you literally cross back into New York! At this point, you are very close to the end.';

let storyWords = story.split(' '); //spilts the string into substrings separated by a space

let unnecessaryWord = 'literally';
let misspelledWord = 'beautifull';
let badWord = 'freaking';
//console.log(storyWords);

//joins the words in the storyWords array based on an empty space character.
//console.log(storyWords.join(' '));

//get a count of all the words in teh storyWords array
let count=0;
//forEach method
storyWords.forEach ((word) => { //callback function
count++;
}); 

//console.log(count);

//filter out all instances of the word literally.
//.filter method
storyWords=storyWords.filter((word) =>{
  return word !==unnecessaryWord; //return any word not equal to the unnecessary word  
});
// .map method

storyWords=storyWords.map((word) =>{
return word===misspelledWord ? 'beutiful' : word;
})
//find the bad word and replace it using findindex
let badWordIndex = storyWords.findIndex((word) =>{
  return word===badWord;
})

storyWords[78]= 'really';
//console.log(badWordIndex);



//find a word longer than 10 characters and replace with a shorte one.
//use every to iterate through the story and check if every word is less than 10 chracters.  Every retunrs true or false.

let lenghtCheck= storyWords.every((word) =>{
  return word.length < 10;

});
console.log(lenghtCheck);
//find a word that's less than 10 characters

storyWords.forEach ((word) =>{
word.length>10 && console.log(word) // find words that are greater than 10 characters and equal the previously identified word.
});

console.log(storyWords.join(' '));









