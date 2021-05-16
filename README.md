# cybot
Simple framework to create conversational telegram bots

## Stage: Idea

## Example:
```ts
async function Home(user: User) {
   const { result: musician } = await ask.text(`Hi ${user.name}! What is your favorite musician?`)
   const { result: song } = await ask.text(`Which song of ${musician} do you like most?`)
   const result = await ask.button(`Do you like ${musician}'s latest album?`, ['Yes', 'No'])
   if (result === 'Yes') {
     // ...
   }
}

bot.command('/start', Home)
```
