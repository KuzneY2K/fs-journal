# CSharp and SQL Fundamentals
01. What is the purpose of a `namespace`?

  > To declare a score that contains related items.

02. What is the difference between a `class` and an `interface`?

  > An interface carries definitions while a class defines and implements those methods. This allows the usage of those methods anywhere in the scope.

03. What is the method that returns an instance of a class, yet it has no return type?

  > a constructor

05. In the Car example what is the access modifier of the `Start()` method?

  ```c#
  abstract class Car
  {
    public string Start()
    {

      return "Vroooom";

    }
  }
  ```

  > Public

06. In the Car example what is `string` an indication of?

  > Type

07. In the Car example what is `abstract` preventing?

  > Code duplication

08. In a SQL table, what is the difference between information in a row and information in a column?

  > The row is a model, the column is the value in that model

09. Demonstrate the necessary SQL for creating a table called `characters` with the values `name, age, description` as strings, and an `int` id.

  > CREATE TABLE
    IF NOT EXISTS characters(
      name VARCHAR(250),
      age VARCHAR(50),
      description VARCHAR(1000),
    )DEFAULT CHARSET UTF8;

  internal Character CreateNewChar(Character characterData){

  string sql = @"
    INSERT INTO characters
    (name, age, descriptions)
    VALUES
    (@name, @age, @description);
  ;";

  Character newChar = _db.Query<Character>(sql, characterData).FirstOrDefault();

  }

10. In SQL how can you query more than a single table? Provide an example.

  > SELECT
    account.*,
    order.*
    FROM orders order
    JOIN customers customer ON order.customerId = account.id
    WHERE order.id = @orderID

