# CustomLuaClass

```lua
class "TestClass" {
  constructor(function(...)
    self.Test = "Hello";
  end);
  Test = {
    Get = function()
        return self.Test
    end;
    Set = function(Value)
      self.Test = Value * 2;
    end;
  };
  Method = function(...)
    print("Test");
  end;
  __mul = function(self, Index)
    return 03000
  end;
  OtherTest = "Value";
}

local Test = new "TestClass" ()

print(Test * 500)
Test:Method()

Test.Test = 4

print(Test.Test)
```
