# Unexpected Behavior When Directly Modifying Instance Variables in Ruby

This example demonstrates a potential issue in Ruby when directly manipulating instance variables using `instance_variable_set` without a corresponding setter method. While you can modify the value, attempts to update it through the intended accessor (the `value` method in this case) will fail to reflect the changes made directly to the instance variable.

This approach may bypass internal logic or validation within the class that would normally occur if the setter method were used, potentially leading to inconsistencies and harder-to-debug problems in larger applications.

**Solution:** Implement a setter method to manage instance variable updates to ensure consistency and maintainability.