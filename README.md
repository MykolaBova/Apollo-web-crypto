---
# Building
<pre>
yarn build
</pre>


---
# Formatting and Linting
We are using Prettier and TsLint!
<pre>
yarn lint
yarn format
</pre>

---
# Tests (with Jest)

In the `src` folder, we have folder called `__tests__`.
Add a new file with a name you like, but it has to end with `test.ts`, for example `FBCrypto.test.ts`

Run tests:
<pre>
yarn test
</pre>

---
# Bumping a new npm package version

Let’s bump a new patch version of the package:
<pre>
npm version patch
</pre>
Our `preversion`, `version`, and `postversion` will run, create a new tag in git and push it to our remote repository. Now publish:
<pre>
npm publish --access=public
</pre>
And now you have a new version.


# Reed-Solomon Encryption

###Implementation

To use the Reed-Solomon encryption, the corresponding cryptographic module can be used. To  set it up, the following steps  should be taken:
    
   1. Import Reed-Solomon encryption functions from  the initial code:
      `import {processAccountIDtoRS, processAccountRStoID} from 'apl-web-crypto';`

   2. Usage:
   
        `const accountRS = processAccountIDtoRS(accountID)`, 
        where `accountID` is user's account id. This function will return account RS value like APL-XXXX-XXXX-XXXX-XXXXX
        
        `const accountID = processAccountRStoID(accountRS)`,
        where `accountRS` is user's account like APL-XXXX-XXXX-XXXX-XXXXX. This function will return account id.

