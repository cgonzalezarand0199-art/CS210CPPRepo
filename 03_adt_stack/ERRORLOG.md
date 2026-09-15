## Error Log

Sep 13, 2026
- Another error was how initially my pop was a void but instead it needed to be an int
  - error: void function 'pop' should not return a value [-Wreturn-mismatch]
    32 |         return value;

Sep 13, 2026
- It wasn't really a compile error, but I did mistakenly put the wrong names for certain call. What I'm referring to when I wanted to push it would do pop and the same the other way around. It took me a while to notice since it didn't mark an error but once I started to test a few time I noticed my mistake.