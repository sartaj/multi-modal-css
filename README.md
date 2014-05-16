# Multi Modal CSS 
### A Corollary to Object Oriented CSS
=========

Object Oriented CSS Principles

### 1. SEPARATION OF STRUCTURE FROM SKIN


### 2. SEPARATION OF CONTAINERS AND CONTENT 


##Corollaries

### 3. Separation of Interaction and Content

### 4. Grouping of Common Properties

When dealing with CSS, a difficult part of maintanence is unifiying common elements together, i.e. typgraphy, padding, layering, etc.

For example, look at this concept

````
	.content {
		font-family: "Open Sans";
	  font-size: 60px;
	  
	  padding: 1em;
	  margin: 1em;
    width: 100%;
    
    z-index: 10;
	}
	
	.content:hover {
	  cursor: pointer;
	 -webkit-overflow-scrolling: touch; 
	}
	
	
````

Instead, separate common properties in the code together, 
````

 /* Typography */
 .content,
 .header {
 		font-family: "Open Sans";
	  font-size: 60px;
 }
 
/* Structure */

  /* padding */

 .content,
 .header,
 {
	  padding: 1em;
 }
 
 /* margin */
 
 .content,
 .header {
     width: 100%;
 }
 
/* Layering */ 
  .header {z-index: 9;}
  .content {z-index: 10;}

/* Interactions */

  /* Mouse */
	.content:hover {
	  cursor: pointer;
	}

  /* Touch */
	.content:hover {
	  	 -webkit-overflow-scrolling: touch; 
	}
	
	
```
