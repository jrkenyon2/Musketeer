# **Musketeer**
 Custom addon for World of Warcraft

The primary purpose of this addon will be to create custom floating nameplates in the gameworld. Other features are planned for the future including a threat meter, dps meter, trash selling, and possibly others.

The primary language is TBD pending more research.

Start Date: 5/25/2022
&nbsp;
## [OAuth](https://www.varonis.com/blog/what-is-oauth) 
  - Blizzard uses OAuth to protect access to data offered through API's. 
  - This is how addons can affect the game client without asking for the users password.
  - OAuth: Open-standard AUTHorization.
  - It allows the sharing of data without the need for passwords.
  - Uses JSON.
  - Philosophy: authorization, not authentication. Selective permission, not full access.
  - Uses a "secret" to verify the source of an access token.
  - OAuth 1.0 is not compatible with 2.0 and is deprecated. (4/5/2012)
  - cURL = confidential URL?
&nbsp;
&nbsp;
## Lua 
  - 1-based indexes
  - Prefers scoped variables to globals of the same name
  - (..) for concatenation
  - code blocks typically use (end) to close. ex: function/end
  - can use (or) for intialization within a function. ex: a = a or 15 (a is set to 15 if the parameter is nil)
&nbsp;
- ### (...) can be used as a parameter for an undetermined amount of arguments
  - when assigning (...) to variables a table should be used (tables replace arrays, lists, etc.)
  - if a table is not used (...) number of parameters will be divided by number of variable (local a,b,c totals 3 variables)
  - assignment of (...) will rotate n times ending with an assignment of the last n parameters to n variables
  - if not evenly divided, the last variable/s will be assigned nil
&nbsp;
- ### hashtables can use variables as keys
  - hashtables have no length
  - built-in iterators ignore hashtable order
&nbsp;
- ### (--[]) creats a comment block
  - (--) is a single line comment
&nbsp;
- ### Loops
  - for/do/end
  - for loops increment by one automatically
  - for loops stop at <=
  - repeat/until is do/while (no 'end' keyword)
  - for/each is for [key, value] /in [iterator]table /do/end
  - no switch/case

&nbsp;
## WoW Developer Portal and Frame UI  
- Sign up for a developer account to get direct access to official documentation - https://www.youtube.com/watch?v=SNdDa4_aN-8 
- You can download interface code and art files to see exposed code showing how the interface is setup - https://www.youtube.com/watch?v=0Z3b0SJuvI0 
- Wow ui is predominantly created through frame commands (objects such as buttons and sliders are categorized as frames through the interface api 
- The most common way to interact with the ui is to attach your code to the parent ui frame (I.e. if I make a new menu element I would add it to the game by adding it to the list of frames registered by the main ui frame through inheritance) 

Interface appears to use xml. Will be learning that before continuing with addon.
