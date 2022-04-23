## It's just a [donut](https://www.a1k0n.net/2011/07/20/donut-math.html)

*Tips :*
*There is a void function called "set_cursor" which prevents the cursor (at least on Windows) from disappearing from the terminal at runtime*

```cpp
void set_cursor(bool visible)
{
	CONSOLE_CURSOR_INFO info;
	info.dwSize = 100;
	info.bVisible = visible;
	SetConsoleCursorInfo(GetStdHandle(STD_OUTPUT_HANDLE), &info);
}
```
<br />

*With set_cursor as true :*
![without](/assets/without_set_cursor.gif)
<br />

*With set_cursor as false :*
![with](/assets/with_set_cursor.gif)
