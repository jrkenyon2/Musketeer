# Musketeer
 Custom addon for World of Warcraft

The primary purpose of this addon will be to create custom floating nameplates in the gameworld. Other features are planned for the future including a threat meter, dps meter, trash selling, and possibly others.

The primary language is TBD pending more research.

Start Date: 5/25/2022


## [OAuth](https://www.varonis.com/blog/what-is-oauth) Notes 6/1
- Blizzard uses OAuth to protect access to data offered through API's. 
- This is how addons can affect the game client without asking for the users password.
- OAuth: Open-standard AUTHorization.
- It allows the sharing of data without the need for passwords.
- Uses JSON.
- Philosophy: authorization, not authentication. Selective permission, not full access.
- Uses a "secret" to verify the source of an access token.
- OAuth 1.0 is not compatible with 2.0 and is deprecated. (4/5/2012)
<br/>
- cURL = confidential URL?
  
  
## Lua notes 6/7
- 1-based indexes
- Prefers scoped variables to globals of the same name
- (..) for concatenation
- code blocks typically use (end) to close. ex: function/end
- can use (or) for intialization within a function. ex: a = a or 15 (a is set to 15 if the parameter is nil)
- ### (...) can be used as a parameter for an undetermined amount of arguments
- when assigning (...) to variables a table should be used (tables replace arrays, lists, etc.)
- if a table is not used (...) number of parameters will be divided by number of variable (local a,b,c totals 3 variables)
- assignment of (...) will rotate n times ending with an assignment of the last n parameters to n variables
- if not evenly divided, the last variable/s will be assigned nil
- ### hashtables can use variables as keys
- hashtables have no length
- built-in iterators ignore hashtable order
  
- ### (--[]) creats a comment block
- (--) is a single line comment
- ### Loops
- for/do/end
- for loops increment by one automatically
- for loops stop at <=
- repeat/until is do/while (no 'end' keyword)
- for/each is for [key, value] /in [iterator]table /do/end
- no switch/case
