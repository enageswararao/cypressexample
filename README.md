  
/*      1.Boolean:
        Represents a boolean value (true or false).
        Example: let isDone: boolean = false;
*/
    let isDone : boolean =true;
    console.log(isDone)

  /*    2.Number:
        Represents numeric values, including integers and floating-point numbers.
        Example: let count: number = 42;
*/
    let num : number = 100
    console.log(num)


 /*    3.String:
        Represents textual data enclosed within single (') or double (") quotes.
        Example: let message: string = "Hello";
 */   
    let message : string = "hello nageswar";
    console.log(message)
 
  /*  4. Array:
        Represents a collection of elements of the same type.
        Example: let numbers: number[] = [1, 2, 3];
  */

    let testArray : number[] = [10,11,12]
    console.log(testArray)
    const arrays : number[] = [1,4,6,7,8,9]
    //older -version
    for (let i = 0; i < arrays.length; i++) {
        const value = arrays[i];
        console.log("Older version .. for loop iteratiing ...."+value)
    }

    //new --version array looping

    // Get an iterator for the array values 
    const iterator = arrays.values()
    // Iterator over the values using a for .. loop 
    for( const value of iterator){
        console.log("for loop iteratiing ...."+value)
    }

  /*   5. Tuple:
        Represents an array-like structure where each element can have its own type.
        Example: let tuple: [string, number] = ["hello", 10];
  */
    let person : [string, number] = ["John",35]
    // Access tuple elements by index
    console.log(person[0]); // Output: John
    console.log(person[1]); // Output: 30
    // Define a tuple with optional elements
    let info: [string, number?] = ["John"];

    // Access tuple elements by index
    console.log(info[0]); // Output: John
    console.log(info[1]); // Output: undefined

    // Define a tuple with rest elements
    let numbers: [number, ...number[]] = [1, 2, 3, 4, 5];

    // Access tuple elements by index
    console.log(numbers[0]); // Output: 1
    console.log(numbers[1]); // Output: 2

    // Access rest of the elements
    console.log(numbers.slice(2)); // Output: [3, 4, 5]

    /* 6.Enum:
        Represents a set of named constants.
    */
        enum Direction {
            Up = 1,
            Down,
            Left,
            Right,
        }
        
        // Access enum values
        console.log(Direction.Up);    // Output: 1
        console.log(Direction.Down);  // Output: 2
        console.log(Direction.Left);  // Output: 3
        console.log(Direction.Right); // Output: 4

        enum Color {
            Red = 'RED',
            Green = 'GREEN',
            Blue = 'BLUE',
        }
        
        // Access enum values
        console.log(Color.Red);    // Output: RED
        console.log(Color.Green);  // Output: GREEN
        console.log(Color.Blue);   // Output: BLUE

        enum LogLevel {
            ERROR,
            WARN,
            INFO,
            DEBUG,
        }
        
        // Access enum keys from values
        console.log(LogLevel[0]); // Output: ERROR
        console.log(LogLevel[1]); // Output: WARN
        console.log(LogLevel[2]); // Output: INFO
        console.log(LogLevel[3]); // Output: DEBUG

        enum Answer {
            Yes = 1,
            No = 'no',
        }
        
        // Access enum values
        console.log(Answer.Yes); // Output: 1
        console.log(Answer.No);  // Output: no

           /* 7.Any:
            Represents a dynamic type that can hold any value.
            Example: let variable: any = 42;
            */
           // Define a variable with the 'any' type
        let data: any;

            // Assign different types of values to the variable
            data = 42;            // Assign a number
            console.log(data);    // Output: 42

            data = 'Hello';       // Assign a string
            console.log(data);    // Output: Hello

            data = true;          // Assign a boolean
            console.log(data);    // Output: true

            data = [1, 'two', true]; // Assign an array with mixed types
            console.log(data);    // Output: [1, 'two', true]

            // Access properties of an 'any' type variable
            let obj: any = { key: 'value' };
            console.log(obj.key); // Output: value

            // Call methods on an 'any' type variable
            let func: any = (x: number, y: number) => x + y;
            console.log(func(2, 3)); // Output: 5

            // Use 'any' type with external libraries or APIs
            // Example: fetching data from an API
            fetch('https://api.example.com/data')
            .then(response => response.json())
            .then((jsonData: any) => {
                // jsonData can be of any type
                console.log(jsonData);
            })
            .catch(error => console.error('Error:', error));

        /*8.Void:
            Represents the absence of a return value.
            Example: function logMessage(): void { console.log("Hello"); }
        */
            function logMessage(): void { console.log("Hello"); }
          /* 9.  Null:
                Represents a null value.
            Example: let data: null = null;
          */
            let data1: null = null;
    /* 10.Undefined:
        Represents an undefined value.
        Example: let data: undefined = undefined;

    */
        : let data2: undefined = undefined;
    /* 11.Never: 
        Represents the type of values that never occur.
        Example: function error(message: string): never { throw new Error(message); }
        
    */
        function error(message: string): never { throw new Error(message); }
      /*  Union:
        Represents a type that can be one of several types.
        Example: let value: string | number;
    */ 
        let value: string | number;

     /*  Type Alias:
        Creates a new name for a type, improving code readability.
        */
       type UserID = string;
       let id : UserID ="1234"
    /* Literal: 
        Represents a specific value rather than a range of values.
        Example: let status: "success" | "error";
    */
        let status2: "success" | "error";
     /**
      *   Object and functions are pending , it is required details ... lot of usage these in automation 
      *   script , we will more details in the next session 
      */
