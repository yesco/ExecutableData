# ExecutableData
Executable Data is data that is universally executable with standardized functions.
When you have the data, the system guarantees that you can interact with that data
in the way that the type of data indicates. If it is an image, it has to be able to
be displayed in a browser using the display method. It doesn't have to be efficient.
And all images must be able to be converted to pbm. Other formats are optional.


There are a number of requirements:
- an ExecutableData has at least one type and *must* implement all the Functions
- a Type has a number of functions
- Data, Types, and Functions have unique IDs and are versioned, and can be tagged
- One can query for latest, or specific version. Types and Functions cannot be removed
- Functions require a working javascript implementation, other languages are optional
- The system can verify each ExecutableData's compliance of the methods
- Data must be a quine, either by identity function, or by implementation of required methods

An image JSON ExecutableData:
```javascript
{
  isED: true,
  types: [exedata://dataist.com/type/
  URI: "data:image/gif;base64,R0lGODlhEAAQAMQAAORHHOVSKudfOulrSOp3WOyDZu6QdvCchPGolfO0o/XBs/fNwfjZ0frl3/zy7////wAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACH5BAkAABAALAAAAAAQABAAAAVVICSOZGlCQAosJ6mu7fiyZeKqNKToQGDsM8hBADgUXoGAiqhSvp5QAnQKGIgUhwFUYLCVDFCrKUE1lBavAViFIDlTImbKC5Gm2hB0SlBCBMQiB0UjIQA7",
  
}
```
