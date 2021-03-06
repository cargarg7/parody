# `Mime`
## Mime provides a simple API for defining and crafting mock classes and objects.

_Copyright (c) 2012 - 2013, Matthew J. Sahagian_.
_Please reference the LICENSE.txt file at the root of this distribution_

### Extends

[`\Dotink\Parody\Quip`](./Quip.md)#### Authors

<table>
	<thead>
		<th>Name</th>
		<th>Handle</th>
		<th>Email</th>
	</thead>
	<tbody>
			<tr>
			<td>
				Matthew J. Sahagian
			</td>
			<td>
				mjs
			</td>
			<td>
				gent@dotink.org
			</td>
		</tr>
	
	</tbody>
</table>

## Properties

### Static Properties

#### <span style="color:#6a6e3d;">$extensions</span>

The list of extension methods and their related callbacks

#### <span style="color:#6a6e3d;">$interfaces</span>

Interfaces for defined classes

#### <span style="color:#6a6e3d;">$parents</span>

Parent class relationships for defined classes

#### <span style="color:#6a6e3d;">$registry</span>

A registry of expanded classes, traits, or interfaces

#### <span style="color:#6a6e3d;">$traits</span>

Traits for defined classes


### Instance Properties
#### <span style="color:#6a6e3d;">$class</span>

The class of the quip that mime is working on

#### <span style="color:#6a6e3d;">$expectation</span>

The current expected arguments of the open Method

#### <span style="color:#6a6e3d;">$quip</span>

A representation of a "pretend" object which is manipulated

#### <span style="color:#6a6e3d;">$openMethod</span>

The currently open method

#### <span style="color:#6a6e3d;">$openProperty</span>

The currently open property



## Methods

### Static Methods
<hr />

#### <span style="color:#3e6a6e;">create()</span>

Create a new quip (mocked object) of a particular class to work on.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$class
			</td>
			<td>
				string
			</td>
			<td>
				The class from which to build the object
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime object for developing the object.
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">define()</span>

Define a new quip (mocked class) to work on.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$class
			</td>
			<td>
				string
			</td>
			<td>
				The class to define
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime object for defining the class
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">make()</span>

Literally makes (evals) a class.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$class
			</td>
			<td>
				string
			</td>
			<td>
				The class to make
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			string
		</dt>
		<dd>
			The qualfied class
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">qualify()</span>

Qualifies a class for the global namespace by ensuring it has a \ in front.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$class
			</td>
			<td>
				string
			</td>
			<td>
				The class to qualify
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			string
		</dt>
		<dd>
			The qualfied class
		</dd>
	
</dl>


### Instance Methods
<hr />

#### <span style="color:#3e6a6e;">__construct()</span>

Create a new Mime.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td rowspan="3">
				$target
			</td>
			<td>
				string
			</td>
			<td rowspan="3">
				A class name or quip to work with.
			</td>
		</tr>
			
		<tr>
			<td>
				object
			</td>
		</tr>
						
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			void
		</dt>
		<dd>
			Provides no return value.
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">__call()</span>

Handle missing calls which, in short, means we should be looking for an extension.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$method
			</td>
			<td>
				string
			</td>
			<td>
				The method we tried to call
			</td>
		</tr>
					
		<tr>
			<td>
				$args
			</td>
			<td>
				array
			</td>
			<td>
				The arguments we passed to it
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">expect()</span>

Tell an open method what to expect

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$arg
			</td>
			<td>
				mixed
			</td>
			<td>
				The expected argument for the mocked method
			</td>
		</tr>
					
		<tr>
			<td>
				$...
			</td>
			<td>
				mixed
			</td>
			<td>
				ad infinitum
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">extending()</span>

Tells the class we're defining to extend a parent class, creating it if it does not
exist.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$parent_class
			</td>
			<td>
				string
			</td>
			<td>
				The parent class to define
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			A new mime for defining the parent
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">give()</span>

Define a value to give for the open method or property

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$value
			</td>
			<td>
				mixed
			</td>
			<td>
				The value to return for the open method or property
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			For method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">implementing()</span>

Tells the class we're defining to implement interfaces, creating it if it does not
exist.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$interface
			</td>
			<td>
				string
			</td>
			<td>
				The interface to implement
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">onCall()</span>

Opens a method on the quip object

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$method
			</td>
			<td>
				string
			</td>
			<td>
				The name of the method to open
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">onGet()</span>

Opens a property on the quip object

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$property
			</td>
			<td>
				string
			</td>
			<td>
				The name of the property to open
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">onNew()</span>

Register a factory for adding methods/property mocks to objects instantiated later.

##### Details

This is useful if the code you are testing has a call such as new Class().  Since the
code is dependent on that object, but it is not injected we essentially want to delay
our method/property configuration for the mock till after that call.  Once the factory
is run it is removed from the stack automatically.

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$arg
			</td>
			<td>
				mixed
			</td>
			<td>
				An optional expected constructor argument
			</td>
		</tr>
					
		<tr>
			<td>
				...
			</td>
			<td>
				mixed
			</td>
			<td>
				
			</td>
		</tr>
					
		<tr>
			<td>
				$callback
			</td>
			<td>
				Closure
			</td>
			<td>
				A callback to be run during construction of the Quip
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">resolve()</span>

Gets the current working quip object (for injection)

###### Returns

<dl>
	
		<dt>
			Quip
		</dt>
		<dd>
			The quip object, whose class will actually be whatever class you're mocking
		</dd>
	
</dl>

<hr />

#### <span style="color:#3e6a6e;">using()</span>

Tell the class we're defining to use a given trait and if it doesn't exist, create it

###### Parameters

<table>
	<thead>
		<th>Name</th>
		<th>Type(s)</th>
		<th>Description</th>
	</thead>
	<tbody>
			
		<tr>
			<td>
				$trait
			</td>
			<td>
				string
			</td>
			<td>
				The trait to use
			</td>
		</tr>
					
		<tr>
			<td>
				$...
			</td>
			<td>
				string
			</td>
			<td>
				ad infinitum
			</td>
		</tr>
			
	</tbody>
</table>

###### Returns

<dl>
	
		<dt>
			Mime
		</dt>
		<dd>
			The mime for method chaining
		</dd>
	
</dl>



