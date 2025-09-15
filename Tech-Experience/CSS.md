### 1. Text ko center karna

```css
p {
  text-align: center;
}
```

### 2. Block element ko horizontally center karna

```css
div {
  width: 200px;
  margin: 0 auto;  /* Left aur right margin auto */
}
```

### 3. Flexbox ka use karke center karna

```css
.container {
  display: flex;
  justify-content: center; /* Horizontal center */
  align-items: center;     /* Vertical center */
  height: 100vh;           /* Pure screen ke beech me */
}
```

### 4. Grid ka use karke

```css
.container {
  display: grid;
  place-items: center;  /* dono (X aur Y) axis me center */
  height: 100vh;
}
```

### 5. Position + Transform se (Absolute Center)

```css
.box {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```