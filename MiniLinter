let story = 'Last weekend, I took literally the most beautiful bike ride of my life. The route is called "The 9W to Nyack" and it actually stretches all the way from Riverside Park in Manhattan to South Nyack, New Jersey. It\'s really an adventure from beginning to end! It is a 48 mile loop and it basically took me an entire day. I stopped at Riverbank State Park to take some extremely artsy photos. It was a short stop, though, because I had a really long way left to go. After a quick photo op at the very popular Little Red Lighthouse, I began my trek across the George Washington Bridge into New Jersey.  The GW is actually very long - 4,760 feet! I was already very tired by the time I got to the other side.  An hour later, I reached Greenbrook Nature Sanctuary, an extremely beautiful park along the coast of the Hudson.  Something that was very surprising to me was that near the end of the route you actually cross back into New York! At this point, you are very close to the end.';

let overusedWords = ['really', 'very', 'basically'];

let unnecessaryWords = ['extremely', 'literally', 'actually' ];

const storyWords = story => story.split(' ')

const wordCount = story =>  storyWords(story).length

//Delete unnecessary words from story array

var betterWords = storyWords(story).filter(word => !unnecessaryWords.includes(word) ) 
  
  //Times overused words were used
function overusedTimes(story) {

  let wordsArray = storyWords(story)
  let counter = new Object

  overusedWords.forEach( word => {
    counter[word] = 0
    for (let i = 0 ; i < wordsArray.length ; i++){
      if (wordsArray[i] === word) {
        counter[word] += 1
      }
    }
  })
  return counter
}


//counts number of sentences in story

const sentenceCount = story => {
  let wordsArray = storyWords(story)
   var count = 0
wordsArray.forEach(word => {
  if (word.includes('!') || word.includes('.')) {
    count++
  }
}) 
return count
}
// argument is any string - returns wordcount, number of sentences and number of times overused words were used
function storyStats(story) {
  console.log(`Wordcount: ${wordCount(story)}`)
 console.log(`Number of sentences: ${sentenceCount(story)}`)
 console.log(`Overused words and number of times used:`)
 console.log(overusedTimes(story))
}

storyStats(story)
var betterStory = betterWords.join(' ')

//remove every other occurance of overused words

function replaceWords(story,overusedArray) {
var replaced = story
  overusedArray.forEach( word => {
    var reg = new RegExp(` ${word}`, "g")
var odd = true
replaced = replaced.replace(reg,word => {
  odd = !odd
  return odd ? "" : word  //change word to replace the overused word
})
   } )
console.log(replaced)

}

replaceWords(betterStory,overusedWords)


//Finds the most used word in the story
//sorts by no. of occurances first then returns last element in array.
function mostTimes(wordArray) {
    return wordArray.sort((a,b) => 
          wordArray.filter(v => v.toLowerCase( )===a.toLowerCase()).length  
       - wordArray.filter(v => v.toLowerCase( )===b.toLowerCase()).length 
    ).pop();
}

console.log(mostTimes(storyWords(story)))



