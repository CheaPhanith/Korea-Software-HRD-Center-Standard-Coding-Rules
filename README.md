# Korea Software HRD Center Standard Coding Rules

<p align="center">
   <img src="https://kshrd.com.kh//static/media/logo.f368c431.png" width="150px"><br>
   <b>HRD CENTER DEVELOPMENT STANDARDS AND GUIDELINES</b>
</p>
<p align="right">
   <b>VERSION 3.0</b><br>
   <b>UPDATED DATE 02/June/2021</b>
</p>
<p align="left">
   <b>Revision History</b>
</p>

| Date   | Version |     Description     |
| ---------- | :---------: | ----------------------- |
| 21/06/2016 |    `1.0`    | Initial Version         |
| 03/08/2020 |    `2.0`    | Update Version          |
| 02/06/2021 |    `3.0`    | Update Version          |

### Table of Contents
Revision History
Table of Contents

1. Introduction
2. Java Rules for Naming
   1. Package
   2. Class
   3. Interface
   4. Method
   5. Variable
   6. Constants
   7. Indentations
   8. Comments
   9. Source Files
   10. Use of Braces
3. Web Rules for Naming
   1. Protocol
   2. HTML (Tag, Attribute…)
   2. CSS (Property)
   3. Javascript (Similar to Java)
   4. ...
4. Coding Guideline
   1. Spacing
   2. Variable Declarations
   3. Program Statements
   4. Use of Parentheses
   5. Meaningful Error Messages
6. Project Folder Structure and Naming Rule(Folder name, File Name)
   1. HTML  
   2. CSS
   3. Javascript
   4. Controller
   5. DAO
   6. Configuration
   7. Example
   8. …
7. Database Naming Rule
   1. Table Name
   2. Field Name
8. Request and Response Format
   1. Request Format
   2. Response Format
   3. Invalid Request Validation Format

## 1. Introduction
In computer programming, a naming convention is a set of rules for choosing the character sequence to be used for identifiers which denote variables, types, functions, and other entities in source code and documentation.

Reasons for using a naming convention (as opposed to allowing programmers to choose any character sequence) include the following:
   * To reduce the effort needed to read and understand source code.
   * To enable code reviews to focus on more important issues than arguing over syntax and naming standards.
   * To enable code quality review tools to focus their reporting mainly on significant issues other than syntax and style preferences.

## 2. Java Rules for Naming
* **Packages** : The prefix of a unique package name is always written in all-lowercase ASCII letters and should be one of the top-level domain names, currently com, edu, gov, mil, net, org, or one of the English two-letter codes identifying countries as specified in ISO Standard 3166, 1981. Subsequent components of the package name vary according to an organization's own internal naming conventions. Such conventions might specify that certain directory name components be division, department, project, machine, or login names.

***Example:***
```java
   com.apple.quicktime.v2
   com.kshrd.ite.exam
   kh.com.kshrd.lumhat
```
   
* **Classes** : Class names should be nouns, in mixed case with the first letter of each internal word capitalized. Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML).

***Example:***
```java
   public class User {
   }
   
   class ExamService {
   }
```
   
* **Interfaces** : Interface names should be capitalized like class names.

***Example:***
```java
   public interface Runnable { 
   }
   
   interface UserMapper {
   }
```
   
* **Methods** : Methods should be verbs, in mixed case with the first letter lowercase, with the first letter of each internal word capitalized.

***Example:***
```java
   public void register(){
   }
   
   private void checkUsernameAndPassword(){
   }
   
   protected int getEmail(){
   }
```
   
* **Variables** : Except for variables, all instance, class, and class constants are in mixed case with a lowercase first letter. Internal words start with capital letters. Variable names should not start with underscore `_` or dollar sign `$` characters, even though both are allowed. Variable names should be short yet meaningful. The choice of a variable name should be mnemonic- that is, designed to indicate to the casual observer the intent of its use. One-character variable names should be avoided except for temporary "throwaway" variables. Common names for temporary variables are `i`, `j`, `k`, `m`, and `n` for integers;  `c`,  `d`, and  `e` for characters.

***Example:***
```java
   int i = 10;
   String address;
   double englishScore;
```

* **Constants** : The names of variables declared class constants and of ANSI constants should be all uppercase with words separated by underscores ("`_`"). (ANSI constants should be avoided, for ease of debugging.)

***Example:***
```java
   static final int MIN_WIDTH = 4;
   static final double PI = 3.14;
   static final String RESPONSE_MESSAGE = "Operation has done";
```
   
* **Indentations** : Indentation should be used to:
   * Emphasize the body of a control statement such as a loop or a select statement 
   * Emphasize the body of a conditional statement 
   * Emphasize a new scope block

* **Comments** : Comment First before start coding.


* **Source file** : Depand on Project Architecture.


* **Use of Braces** : Comment First before start coding.  
Even Though the single line of could should use the braces

***Example:***
```java
   if(condition){
       
   }
   
   Or 
   
   if(condition)
   {
   
   }
```
## 3. Web Rules for Naming: General style rules for HTML, CSS, JavaScript
* **Protocol** 
    * Protocol: Use the HTTPS protocol for embedded resources where possible.  

      Always use the HTTPS protocol ( https: ) for images and other media files, style sheets and scripts, unless the respective files are not available over HTTPS.

      ```html
      <!-- Recommended -->
      <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
      ```
      ```javascript
      /* Recommended */
      @import 'https://fonts.googleapis.com/css?family=Open+Sans';
      ```  

* **General Formatting Rules** 
    * Indentation: Indent by 2 spaces at a time or a tab at a time.  

      ```html
      <ul>
        <li>Fantastic
        <li>Great
      </ul>
      ```
     * Capitalization: Use only lowercase.

       All code has to be lowercase: This applies to HTML element names, attributes, attribute values (unless text/CDATA), CSS selectors, properties, and property values (with the exception of strings).   
     
       ```html
      <!-- Recommended -->
      <img src="google.png" alt="Google">
       ```
       ```javascript
      /* Recommended */
      color: #e5e5e5;
       ```
* **General Meta Rules** 
     * Encoding  

       Use UTF-8 (no BOM).

       Make sure your editor uses UTF-8 as character encoding, without a byte order mark.

       Specify the encoding in HTML templates and documents via <b><meta charset="utf-8"></b>. Do not specify the encoding of style sheets as these assume UTF-8.
       
     * Comments  
       
       Explain code as needed, where possible.
            
       Use comments to explain code: What does it cover, what purpose does it serve, why is respective solution used or prefered?
 
       (This item is optional as it is not deemed a realistic expectation to always demand fully documented code. Mileage may vary heavily for HTML and CSS code and depends on the project’s complexity.)

     * Action Items

       Mark todos and action items with <b>TODO</b>.
 
       Highlight todos by using the keyword <b>TODO</b> only, not other common formats like <b>@@</b>.
 
       Append a contact (username or mailing list) in parentheses as with the format <b>TODO(contact)</b>.
 
       Append action items after a colon as in <b>TODO: action item</b>.

       ```html
       {# TODO(john.doe): revisit centering #}
       <center>Test</center>
       ```
       ```html
       <!-- TODO: remove optional tags -->
       <ul>
         <li>Apples</li>
         <li>Oranges</li>
       </ul>
       ```

* **HTML** 
    * Document Type: Use HTML5.  
      
      HTML5 (HTML syntax) is preferred for all HTML documents: <b>\<!DOCTYPE html\></b>  
            
    * HTML Validity: Use valid HTML where possible.  
      
      Use valid HTML code unless that is not possible due to otherwise unattainable performance goals regarding file size.

      Using valid HTML is a measurable baseline quality attribute that contributes to learning about technical requirements and constraints, and that ensures proper HTML usage.
      
       ```html
       <!-- Recommended -->
       <!DOCTYPE html>
       <meta charset="utf-8">
       <title>Test</title>
       <article>This is only a test.</article>
       ```
    * Semantics.
            
    * Use HTML according to its purpose..  
      
      Use elements (sometimes incorrectly called “tags”) for what they have been created for. For example, use heading elements for headings, p elements for paragraphs, a elements for anchors, etc
      
      Using HTML according to its purpose is important for accessibility, reuse, and code efficiency reasons.
       ```html
       <!-- Recommended -->
       <a href="recommendations/">All recommendations</a>
       ```
       
    * Multi media fallback  
      
      Provide alternative contents for multimedia.
      
      For multimedia, such as images, videos, animated objects via `canvas`, make sure to offer alternative access. For images that means use of meaningful alternative text (`alt`) and for video and audio transcripts and captions, if available.
      
      Providing alternative contents is important for accessibility reasons: A blind user has few cues to tell what an image is about without `@alt`, and other users may have no way of understanding what video or audio contents are about either.
      
      (For images whose `alt` attributes would introduce redundancy, and for images whose purpose is purely decorative which you cannot immediately use CSS for, use no alternative text, as in `alt=""`.)
       ```html
       <!-- Recommended -->
       <img src="spreadsheet.png" alt="Spreadsheet screenshot.">
       ```
    * Separated Concern  
      
      Separate structure from presentation from behavior.
      
      Strictly keep structure (markup), presentation (styling), and behavior (scripting) apart, and try to keep the interaction between the three to an absolute minimum.
      
      That is, make sure documents and templates contain only HTML and HTML that is solely serving structural purposes. Move everything presentational into style sheets, and everything behavioral into scripts.
      
      In addition, keep the contact area as small as possible by linking as few style sheets and scripts as possible from documents and templates.
      
      Separating structure from presentation from behavior is important for maintenance reasons. It is always more expensive to change HTML documents and templates than it is to update style sheets and scripts.
       ```html
       <!-- Not recommended -->
       <!DOCTYPE html>
       <title>HTML sucks</title>
       <link rel="stylesheet" href="base.css" media="screen">
       <link rel="stylesheet" href="grid.css" media="screen">
       <link rel="stylesheet" href="print.css" media="print">
       <h1 style="font-size: 1em;">HTML sucks</h1>
       <p>I’ve read about this on a few sites but now I’m sure:
       <u>HTML is stupid!!1</u>
       <center>I can’t believe there’s no way to control the styling of
       my website without doing everything all over again!</center>
       ```
       ```html
       <!-- Recommended -->
       <!DOCTYPE html>
       <title>My first CSS-only redesign</title>
       <link rel="stylesheet" href="default.css">
       <h1>My first CSS-only redesign</h1>
       <p>I’ve read about this on a few sites but today I’m actually
        doing it: separating concerns and avoiding anything in the HTML of
        my website that is presentational.
       <p>It’s awesome!
       ```
    * Entity Reference  
      
      Do not use entity references.
      
      There is no need to use enntity references like `&mdash;`, `&rdquo;`, or `&#x263a;`, assuming the same encoding (UTF-8) is used for files and editors as well as among teams.
      
      The only exceptions apply to characters with special meaning in HTML (like `<` and `&`) as well as control or “invisible” characters (like no-break spaces).  
       ```html
       <!-- Not recommended -->
       The currency symbol for the Euro is &ldquo;&eur;&rdquo;.
       ```
       ```html
       <!-- Recommended -->
       The currency symbol for the Euro is “€”.
       ```
       
    * Type Attributes 
      
      Omit `type` attributes for style sheets and scripts.
      
      Do not use `type` attributes for style sheets (unless not using CSS) and scripts (unless not using JavaScript).
      
      Specifying type attributes in these contexts is not necessary as HTML5 implies [text/css](https://whatwg.org/specs/web-apps/current-work/multipage/semantics.html#attr-style-type) and [text/javascript](https://whatwg.org/specs/web-apps/current-work/multipage/scripting.html#attr-script-type) as defaults. This can be safely done even for older browsers.
       ```html
       <!-- Recommended -->
       <link rel="stylesheet" href="https://www.google.com/css/maia.css">
       ```
    
        * HTML Quotation Marks  
          When quoting attributes values, use double quotation marks.
      
          Use double (`""`) rather than single quotation marks (`''`) around attribute values.
          ```html
          <!-- Recommended -->
          <a class="maia-button maia-button-secondary">Sign in</a>
          ```
* **CSS** 
    * CSS Style Rules
        * Validity 
          Use valid CSS where possible.
      
          Unless dealing with CSS validator bugs or requiring proprietary syntax, use valid CSS code.
      
          Using valid CSS is a measurable baseline quality attribute that allows to spot CSS code that may not have any effect and can be removed, and that ensures proper CSS usage.
          
        * ID and Class Naming 
          Use meaningful or generic ID and class names.
      
          Instead of presentational or cryptic names, always use ID and class names that reflect the purpose of the element in question, or that are otherwise generic.
      
          Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change.
          
          Generic names are simply a fallback for elements that have no particular or no meaning different from their siblings. They are typically needed as “helpers.”
          
          Using functional or generic names reduces the probability of unnecessary document or template changes.

          ```css
          /* Recommended: specific */
          #gallery {}
          #login {}
          .video {}
          ```
          ```css
          /* Recommended: generic */
          .aux {}
          .alt {}
          ```
        * ID and Class Name Style
          Use ID and class names that are as short as possible but as long as necessary.
      
          Try to convey what an ID or class is about while being as brief as possible.
      
          Using ID and class names this way contributes to acceptable levels of understandability and code efficiency.

          ```css
          /* Not recommended */
          #navigation {}
          .atr {}
          ```
          ```css
          /* Recommended */
          #nav {}
          .author {}
          ```
        * Type Selectors
          Avoid qualifying ID and class names with type selectors.
      
          Unless necessary (for example with helper classes), do not use element names in conjunction with IDs or classes.
      
          Avoiding unnecessary ancestor selectors is useful for [performance reasons](http://www.stevesouders.com/blog/2009/06/18/simplifying-css-selectors/).

          ```css
          /* Not recommended */
          ul#example {}
          div.error {}
          ```
          ```css
          /* Recommended */
          #example {}
          .error {}
          ```
        * Shorthand Properties
          Use shorthand properties where possible.
      
          CSS offers a variety of [shorthand](https://www.w3.org/TR/CSS21/about.html#shorthand) properties (like `font`) that should be used whenever possible, even in cases where only one value is explicitly set.
      
          Using shorthand properties is useful for code efficiency and understandability.

          ```css
          /* Not recommended */
          border-top-style: none;
          font-family: palatino, georgia, serif;
          font-size: 100%;
          line-height: 1.6;
          padding-bottom: 2em;
          padding-left: 1em;
          padding-right: 1em;
          padding-top: 0;
          ```
          ```css
          /* Recommended */
          border-top: 0;
          font: 100%/1.6 palatino, georgia, serif;
          padding: 0 1em 2em;
          ```
        * 0 and Units
          Omit unit specification after “0” values, unless required.  
          Do not use units after 0 values unless they are required.

          ```css
          flex: 0px; /* This flex-basis component requires a unit. */
          flex: 1 1 0px; /* Not ambiguous without the unit, but needed in IE11. */
          margin: 0;
          padding: 0;
          ```
        * Leading 0s
          Omit leading “0”s in values.  
          Do not use put `0`s in front of values or lengths between -1 and 1.

          ```css
          font-size: .8em;
          ```
        * Hexadecimal Notation
          Use 3 character hexadecimal notation where possible.  
          For color values that permit it, 3 character hexadecimal notation is shorter and more succinct.

          ```css
          /* Recommended */
          color: #ebc;
          ```
        * Prefixes
          for code that gets embedded in other projects or on external sites use prefixes (as namespaces) for ID and class names. Use short, unique identifiers followed by a dash.
          
          Using namespaces helps preventing naming conflicts and can make maintenance easier, for example in search and replace operations.

          ```css
          .adw-help {} /* AdWords */
          #maia-note {} /* Maia */
          ```
        * ID and Class Name Delimiters
          Separate words in ID and class names by a hyphen.
          
          Do not concatenate words and abbreviations in selectors by any characters (including none at all) other than hyphens, in order to improve understanding and scannability.

          ```css
          /* Recommended */
          #video-id {}
          .ads-sample {}
          ```
        * Hacks
          Avoid user agent detection as well as CSS “hacks”—try a different approach first.
          
          It’s tempting to address styling differences over user agent detection or special CSS filters, workarounds, and hacks. Both approaches should be considered last resort in order to achieve and maintain an efficient and manageable code base. Put another way, giving detection and hacks a free pass will hurt projects in the long run as projects tend to take the way of least resistance. That is, allowing and making it easy to use detection and hacks means using detection and hacks more frequently—and more frequently is too frequently.

    * CSS Formatting Rules
        * Declaration Order
          Alphabetize declarations.
      
          Put declarations in alphabetical order in order to achieve consistent code in a way that is easy to remember and maintain.
      
          Ignore vendor-specific prefixes for sorting purposes. However, multiple vendor-specific prefixes for a certain CSS property should be kept sorted (e.g. -moz prefix comes before -webkit).

          ```css
          background: fuchsia;
          border: 1px solid;
          -moz-border-radius: 4px;
          -webkit-border-radius: 4px;
          border-radius: 4px;
          color: black;
          text-align: center;
          text-indent: 2em;
          ```
        * Block Content Indentation
          Indent all block content.
      
          Indent all [block content](https://www.w3.org/TR/CSS21/syndata.html#block), that is rules within rules as well as declarations, so to reflect hierarchy and improve understanding.

          ```css
          @media screen, projection {
            html {
              background: #fff;
              color: #444;
            }
          }
          ```
        * Declaration Stops
          Use a semicolon after every declaration.
      
          End every declaration with a semicolon for consistency and extensibility reasons.

          ```css
          /* Not recommended */
          .test {
            display: block;
            height: 100px
          }
          ```
          ```css
          /* Recommended */
          .test {
            display: block;
            height: 100px;
          }
          ```
        * Property Name Stops
          Use a space after a property name’s colon.
      
          Always use a single space between property and value (but no space between property and colon) for consistency reasons.

          ```css
          /* Not recommended */
          h3 {
            font-weight:bold;
          }
          ```
          ```css
          /* Recommended */
          h3 {
            font-weight: bold;
          }
          ```
        * Declaration Block Separation
          Use a space between the last selector and the declaration block.
      
          Always use a single space between the last selector and the opening brace that begins the [declaration block](https://www.w3.org/TR/CSS21/syndata.html#rule-sets
          
          The opening brace should be on the same line as the last selector in a given rule.

          ```css
          /* Not recommended: missing space */
          #video{
            margin-top: 1em;
          }

          /* Not recommended: unnecessary line break */
          #video
          {
            margin-top: 1em;
          }
          ```
          ```css
          /* Recommended */
          #video {
            margin-top: 1em;
          }
          ```
        * Declaration Block Separation
          Separate selectors and declarations by new lines.
      
          Always start a new line for each selector and declaration.

          ```css
          /* Not recommended */
          a:focus, a:active {
            position: relative; top: 1px;
          }
          ```
          ```css
          /* Recommended */
          h1,
          h2,
          h3 {
            font-weight: normal;
            line-height: 1.2;
          }
          ```
        * Rule Separation
          Separate rules by new lines.
      
          Always put a blank line (two line breaks) between rules.

          ```css
          html {
            background: #fff;
          }

          body {
            margin: auto;
            width: 50%;
          }
          ```
        * CSS Quotation Marks
          Use single quotation marks for attribute selectors and property values.
      
          Use single (`''`) rather than double (`""`) quotation marks for attribute selectors or property values. Do not use quotation marks in URI values (`url()`).
          
          Exception: If you do need to use the `@charset rule`, use double quotation marks—[single quotation marks are not permitted](https://www.w3.org/TR/CSS21/syndata.html#charset).

          ```css
          /* Not recommended */
          @import url("https://www.google.com/css/maia.css");

          html {
            font-family: "open sans", arial, sans-serif;
          }
          ```
          ```css
          /* Recommended */
          @import url(https://www.google.com/css/maia.css);

          html {
            font-family: 'open sans', arial, sans-serif;
          }
          ```
    * CSS Meta Rules
        * Section Comments
          Group sections by a section comment (optional).
      
          If possible, group style sheet sections together by using comments. Separate sections with new lines.

          ```css
          /* Header */

          #adw-header {}

          /* Footer */

          #adw-footer {}

          /* Gallery */

          .adw-gallery {}
          ```
* **ReactJS**
    * **Naming Rules**
      * CapitalLetter: class/function components which return JSX and extension (.jsx) and CSS files
      * camelCase: reusable function without return JSX and extension (.js)
      * lowercase: apply all folder structures
    
    * **Folder Structures**
      * /public/images: image assets should be stored in public folder
      * /src/styles: each component styles should be stored in styles folder and App.css for  global style.
      * /src/components: all reusable components(Navbar...)
      * /src/views: all small pages components(Home, About...)
      * /src/services: store BASEURL or reusable function with api
      * /src/redux: contain /actions, /reducers, /store which related to STATE Management
      

#### **Parting Words**
Be consistent.

If you’re editing code, take a few minutes to look at the code around you and determine its style. If they use spaces around all their arithmetic operators, you should too. If their comments have little boxes of hash marks around them, make your comments have little boxes of hash marks around them too.
 
The point of having style guidelines is to have a common vocabulary of coding so people can concentrate on what you’re saying rather than on how you’re saying it. We present global style rules here so people know the vocabulary, but local style is also important. If code you add to a file looks drastically different from the existing code around it, it throws readers out of their rhythm when they go to read it. Avoid this.

* **JavaScript Naming** 
    * Note: The similar to  Java Programming language.

## 4. Coding Guideline
* **Spacing**  
The proper use of spaces within a line of code can enhance readability. Good rules of thumb are as follows: 
    * A keyword followed by a parenthesis should be separated by a space.
    * A blank space should appear after each comma in an argument list.
    * All binary operators except “.” should be separated from their operands by spaces. Blank spaces should never separate unary operators such as unary minus, increment (“++”), and decrement(“—“) from their operands. 
    * Casts should be made followed by a blank space.

  ***Example:***  

  ```java
  Bad: 
  cost=price+(price*sales_tax);  
  ```
  ```java
  Better: 
  cost = price + (price * sales_tax);
  ```
* **Variable Declaration** : Variable declarations that span multiple lines should always be preceded by a type.  

  ***Example:***  

  ```java
  Acceptable: 
  int price, score; 

  Acceptable: 
  int price; 
  int score; 
  ```
  ```java
  Not Acceptable: 
  int price, 
      score; 
  ```
* **Program Statement** : Program statements should be limited to one per line. Also, nested statements should be avoided when possible.  

  ***Example:***

  ```java
  Bad: 
  number_of_names = names.length ; b = new JButton [number_of_names]; 
  ```
  ```java
  Better: 
  number_of_names = names.length; 
  b = new JButton [number_of_names];
  ```
* **Use of Parentheses** : It is better to use parentheses liberally. Even in cases where operator precedence unambiguously dictates the order of evaluation of an expression, often it is beneficial from a readability point of view to include parentheses anyway.  

  ***Example:***

  ```java
  Acceptable: 
  total = 3 – 4 * 3; 

  Better: 
  total = 3 – (4 * 3);

  Even better: 
  total = (-4 * 3) + 3; 
  ```
  ***Example:***
  ```java
  Acceptable: 
  if (a == b && c == d) 
  Better: 
  if ((a == b) && (c == d)) 
  ```
* **Meaningful Error Messages** : Error messages should be meaningful. When possible, they should indicate.
    * what the problem is, 
    * where the problem occurred, 
    * and when the problem occurred.


## 5. Project Folder Structure and Naming Rule(Folder name, File Name)
#### Sample FIle 

File Documentation Block Definition:  
This documentation block is located at the beginning of the file.
```java
/********************************************************************** 
* Original Author: 
* Created Date:
* Development Group:
* Description: 
 **********************************************************************/ 
public class ClassName {
 
/********************************************************************** 
* Original Author: 
* Created Date:
* Description: 
*         TODO: 
* Parameters:
*      Name     Type       Description
*      score    double     The score of the student to be checked.
*
* Return Value:
*      Type     Description
*      String   The rank of the student.
* Error Codes/ Exceptions:
*      SCORE_LOWER_THAN_ZERO The score lower than zero
* Local Variable
*      Name     Type       Description
* Modification History
*      Date     Developer  Description        
* 
***********************************************************************/ 
   public String checkScore(double score) {
      
   } 
}
```

#### Example class:
```java
/********************************************************************** 
* Author: 
* Created Date:
* Development Group:
* Description: 
**********************************************************************/ 
public class ClassName {
      /********************************************************************** 
      * Original Author: 
      * Created Date:
      * Description: 
      * Modification History
      *     Date: 
      *  Developer: 
      *  TODO: 
      **********************************************************************/ 
      public String checkScore(double score) {

      }
}
```

## 6. Database Naming Rule
* Collation: UTF-8
* DO NOT USE “double quotes” because it will make the object CASE SENSITIVE.


* Object: Using underscore for word separating (e.g. v_show_active_user)
    * View
      *  Prefix {v_}
    * Trigger
      *  Prefix {tr_}
    * Procedure
      *  Prefix {pr_}
    * Function
      *  Prefix {f_}
* Table
    * Prefix: {Database’s Name Abbreviation which is provided by mentor}
    * NO “TBL” prefix
    * Using underscore for word separating (e.g. exp_expert_information)
    * Table name should be specified in plural noun (e.g. stm_students)
* Column
    * Using lowercase
    * Using underscore for word separating (e.g. login_history)
* ID Field
    * Datatype: serial
* SQL Statement
    * Use Uppercase for SQL’s keywords and lowercase for object name
    * Do not use * to select data, especially when selecting with joining table
    * Specify the name of column when Insert or select data.

```sql
(SELECT id, name, gender FROM stm_students;
 INSERT INTO stm_students(name, gender) VALUES(‘my name’, ‘male’);)
```

## 7. Request and Response Data Format
* Request Data

```json
{
   "accessToken": "$2a$10$/uoQZ1oeJh3GgRt8nEd.U.uohK14UJnL9X45cfO2EzIG0VVF2lIDi",
   "data": {
      "name": "KSHRD CENTER",
      "address": "Kandal",
      "phoneNumber": "012345678"
   }
}
```
or
```json
{
   "username": "instructor",
   "password": "123456789"
}
```
or
```json
{
   "firstName": "Sok",
   "lastName": "Dara",
   "email": "sokdara9999@gmail.com",
   "password": "99991010",
   "roles": [
     {"id":1},
     {"id":2}
   ],
   "education": {
     "major": "Computer Egineering",
     "university": "RUPP",
     "degree": "Master"
   }
}
```

* Response Data
    * Response Data with a object
    
```json
{
   "code": 200,
   "message": "User has been found successfully",
   "requestedTime": "2021-06-02T02:52:38.631+00:00",
   "data": {
      "id": 1,
      "displayName": "Chan Dara",
      "gender": "Male",
      "email": "chandarakhmer@gmail.com"
   }
}
```

   * Response Data with list

```json
{
   "code": 200,
   "message": "Users have been found successfully",
   "requestedTime": "2021-06-02T02:52:38.631+00:00",
   "data": [
      {
        "id": 2,
        "displayName": "Kok Dara",
        "gender": "Male",
        "email": "mrkokdara@hotmail.com"
      },
      {
        "id": 1,
        "displayName": "Chan Dara",
        "gender": "Male",
        "email": "chandarakhmer@gmail.com"
      }
   ],
   // Pagination is optional. If you need to use it, you can response this object for handling in UI (Web or Mobile App).
   "pagination": {
        "page": 1,
        "limit": 15,
        "nextPage": 1,
        "previousPage": 1,
        "totalCount": 9,
        "totalPages": 1,
        "pagesToShow": 6,
        "startPage": 1,
        "endPage": 1,
        "offset": 0
    }
}
```

   * Invalid Request Validation

```json
{
   "code": 400,
   "message": "Invalid request on update user information",
   "requestedTime": "2021-06-02T02:52:38.631+00:00",
   "errors": {
     "message": "JSON parse error: Unexpected character ('\"' (code 34)): was expecting comma to separate Object entries"
   }
}
```
or
```json
{
   "code": 400,
   "message": "Invalid request on add a new user",
   "requestedTime": "2021-06-02T02:52:38.631+00:00",
   "errors": [
      {
         "field": "Username",
         "message": "Username must not be blank"
      },
      {
        "field": "Password",
        "message": "Password doesn't match"
      }
   ]
}
```
