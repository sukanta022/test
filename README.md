<b>4) How can you share state between components in React?</b><br>
Ans: Using Lift Up State, it passes the data from parent component to child component. For example:<br>
<br>
<code>
const Parent = () =&gt; {<br>
&nbsp;&nbsp;const [count, setCount] = useState(0);<br>
&nbsp;&nbsp;return (<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;ChildA count={count} /&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;ChildB setCount={setCount} /&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt;<br>
&nbsp;&nbsp;);<br>
};<br>
</code>

<br><br>

<b>5) How is event handling done in React?</b><br>
Ans: Event handling is done in React using the event attribute <code>onClick</code>. Instead of calling it, we pass the function as an event handler. For example:<br>
<br>

<code>
function App() {<br>
&nbsp;&nbsp;function handleClick() {<br>
&nbsp;&nbsp;&nbsp;&nbsp;alert("Button clicked!");<br>
&nbsp;&nbsp;}<br>
<br>
&nbsp;&nbsp;return (<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;button onClick={handleClick}&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Click Me<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/button&gt;<br>
&nbsp;&nbsp;);<br>
}<br>
</code>

<br>
When passing data inside the event handler, we use an arrow function to prevent immediate execution. For example:<br>
<br>

<code>
function App(data) {<br>
&nbsp;&nbsp;function handleClick() {<br>
&nbsp;&nbsp;&nbsp;&nbsp;alert(data);<br>
&nbsp;&nbsp;}<br>
<br>
&nbsp;&nbsp;return (<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;button onClick={() =&gt; {handleClick(data)}}&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Click Me<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/button&gt;<br>
&nbsp;&nbsp;);<br>
}<br>
</code>
