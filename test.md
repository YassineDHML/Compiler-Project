# Compiler Playground Test Payloads

These payloads were sent to the `/api/run` endpoint as JSON:

```json
{"source": "<payload>"}
```

## Payloads

### 1) Simple declaration
```
int x;
```

### 2) Declaration + arithmetic assignment
```
int x;
x = 5 + 2;
```

### 3) String declaration + assignment + concat
```
string name;
name = "hello";
name = "hello" + " world";
```

### 4) Duplicate declaration (semantic error)
```
int x;
int x;
```

### 5) Undeclared variable assignment (semantic error)
```
y = 10;
```

### 6) Type mismatch assignment (semantic error)
```
int x;
x = "oops";
```

### 7) Mixed-type binary op (semantic error)
```
int x;
x = 1 + "bad";
```

### 8) Missing semicolon (parser error)
```
int x
x = 5;
```

### 9) If statement (no else)
```
int x;
x = 5;
if (x > 3) { x = 6; }
```

### 10) If/else statement
```
int x;
if (x > 0) { x = 1; } else { x = 2; }
```
