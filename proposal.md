Keeping things all on a single line is confusing and limiting. An expectation on an element can enforce multiple things, such as attributes:

    element 'logger' hasAttribute 'category' hasAttribute 'level'

This works fine for simple cases but can quickly escale and cause confusion when dealing with additional criteria:

    element 'logger' hasAttribute 'category' with value: having a property hasAttribute 'level'

It doesn't make it clear the `having a proerty` is for the 'category' or 'level'. This can continue to get unwieldy.

    element 'logger' hasAttribute 'category' with value: having a property hasAttribute 'level' with value: having a property

A period, or colon, or otherwise syntacial sugar can be placed to break it up and make it clear, but a new line character can perform this same function


element 'logger' {
  attribute 'category'
  attribute 'level'
}

element 'logger' {
  attribute 'category' {
    value is a property
  }

  attribute 'level' {
    value is a property
  }
}

It takes up 9 lines, but does make it easier to logically group items together and know where their scope begins or ends and how things tie together

The original DSL was meant to read [similar] to a sentance and be flowing. I don't think this will be reasonable as we continue to add specific rules/expectations/criteria.

Nested scope - In the case of setting a rule for the "Client" attribute of a HTTP call (or any other header) - this would need to be taken care of in a nested manner.
    Element XYZ has child, which has child ...etc which has attribute Client with value Y

    
# TODO Not sure I want to say this
Excluding rules from a file or path is also often requested. These could be a standalone line with the current syntax, but 

##### Answer: the question on what if the start of each sentance was different?
Currently - when starting each sentance the context is lost as to what element or attribute it is tied to (a made up example):

    element 'logger' hasAttribute 'level' hasAttribute 'category'
    attribute 'level' is lower cased
    attribute 'category' is upper cased

Following this approach the DSL logic would need to remember state across multiple sentances. Carrying around the state is something I fear would introduce bugs and make it harder to expain upon the venacular of the DSL.

Using closures in Groovy, we can introduce a way to "scope" items a bit better by using the owner/delegate/this
TODO Which is it?
    element 'logger' hasAttribute 'level' hasAttribute 'category' {
        attribute 'level' is lower cased
        attribute 'category' is upper cased
    }