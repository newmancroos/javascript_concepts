# javascript_concepts

<h2>Scopes and Closures</h2>
<p>
    In javascript we can write function in three different ways<br/>
    <ul>
        <li>
            <pre>
                function foo(){
                    console.log("Function foo called");
                }
            </pre>
        </li>
        <li>
            <pre>
                var foo = function(){
                    console.log("Function foo Called");
                }
            </pre>
        </li>
        <li>
            <pre>
                foo = () =&gt; {
                    console.log("Function foo called");
                }
            </pre>
        </li>
    </ul>
    <p>
        in javascript block is made off of functions.
        <pre>
            var name = "Newman";
            if(name === "Newman")
            {
                var department = "IT";
            }
            console.log(name);   // Output is Newman
            console.log(department);  // Output is IT
        </pre>
        here if block does not create any scope in javascript.
    </p>
    <p>
        <pre>
            var newman = "Newman";
            function allocateDepartment(){
                if(name === "Newman")
                {
                    var department = "IT";
                }
            }
            allocateDepartment(); //Output is IT
            console.log(name);  //Output is Newman
            consle.log(department);   // Error out of scope
        </pre>
    </p>
	<p>
		<u>ES6/7/8</u>
<br>
<br>
		- var / let   <br>
		- const 
		- funtion a()  <changed to> const a = function(){}  <changed to> a = () =>{} <br>
		- string manupolation $`{variablname}' <br>
		- Destructing -> const [one, two, three] = array;   (array = [1,2,3])<br>
			console.log(one)   (1 --- Array destruction)<br>
			var a = {age : 8, school: "test"}; ag = a.age; sc = a.school; (object destrction - Es5)<br>
			const {age, school} = a;<br>
		-Spread operator<br>
			const family = ['list','Bart']<br>
			const pet = ['dog','cat']<br>
			const all = [...family, ...pet]; //'list','bart','dog','cat'<br>
<br>
		-Object.values  - takes object as input and return array as outpt<br>
				const character = {name : 'Lisa', age : 8, school: 'test'}<br>
				console.log(Object.values(character))  //['Lisa','8', 'test']<br>
		-Object.entries - takes object as input and return array as keyvalue paire<br>
				console.log(Object.entries(character))   // [[name: 'Lisa'], [age:8], [school:'test']]<br>
		-string.padEnd(length,string)<br>
				concatinate string with string untile spcified length. if length is more string will repeated<br>
				'The'.padEnd(10) // 'The          '<br>
				'The'.padEnd(10, 'newmancroos') //'10newmancroo'<br>
				'The'.pdEnd(20, 'newmancroos') //'10newmancroosnewmancroosne'<br>
		-string.padStart(length,string)    //same as string.padEnd but concatinate in the front of the first string<br>
<br>
		-array.flat(optional dept)<br>
				this will flatten the array as flat element and we can specfy how deep we have to traverse in child array<br>
				const array = [1,2,3,[4,5]]<br>
				console.log(array.flat(1))   // [1,2,3,4,5]<br>
				const array = [1,2,[3,[4,5]]]<br>
				array.flat(1)  // [1,2,3,[4,5]]<br>
<br>
		- array.flatMap <br>
				* It does flat and map operations<br>
			const array = [1,2,3,4,5]<br>
			var arr = array.map(x => [x*2])  // [[2],[4],[6],[8],[10]]<br>
			arr.flat() ; [2,4,6,8,10]<br>
<br>
			array.flatMap( x => [x * 2])) // [2,4,6,8,10]<br>
<br>
		- fromEntries transforms a list of key-value paire into an object<br>
			const listArray = [<br>
					['grade',2],<br>
					['school','test school']<br>
				]<br>
			console.log(Object.fromEntries(listArray))   //{grade:2, school: 'test school'}<br>
		-trimStart / trimEnd   - trim start and end whitespace<br>
	<br>
	<br>
	</p>
</p>