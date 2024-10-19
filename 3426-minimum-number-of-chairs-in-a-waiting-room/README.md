<h2><a href="https://leetcode.com/problems/minimum-number-of-chairs-in-a-waiting-room">3426. Minimum Number of Chairs in a Waiting Room</a></h2><h3>Easy</h3><hr><p>You are given a string <code>s</code>. Simulate events at each second <code>i</code>:</p>

<ul>
	<li>If <code>s[i] == &#39;E&#39;</code>, a person enters the waiting room and takes one of the chairs in it.</li>
	<li>If <code>s[i] == &#39;L&#39;</code>, a person leaves the waiting room, freeing up a chair.</li>
</ul>

<p>Return the <strong>minimum </strong>number of chairs needed so that a chair is available for every person who enters the waiting room given that it is initially <strong>empty</strong>.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<div class="example-block">
<p><strong>Input:</strong> <span class="example-io">s = &quot;EEEEEEE&quot;</span></p>

<p><strong>Output:</strong> <span class="example-io">7</span></p>

<p><strong>Explanation:</strong></p>

<p>After each second, a person enters the waiting room and no person leaves it. Therefore, a minimum of 7 chairs is needed.</p>
</div>

<p><strong class="example">Example 2:</strong></p>

<div class="example-block">
<p><strong>Input:</strong> <span class="example-io">s = &quot;ELELEEL&quot;</span></p>

<p><strong>Output:</strong> <span class="example-io">2</span></p>

<p><strong>Explanation:</strong></p>

<p>Let&#39;s consider that there are 2 chairs in the waiting room. The table below shows the state of the waiting room at each second.</p>
</div>

<table>
	<tbody>
		<tr>
			<th>Second</th>
			<th>Event</th>
			<th>People in the Waiting Room</th>
			<th>Available Chairs</th>
		</tr>
		<tr>
			<td>0</td>
			<td>Enter</td>
			<td>1</td>
			<td>1</td>
		</tr>
		<tr>
			<td>1</td>
			<td>Leave</td>
			<td>0</td>
			<td>2</td>
		</tr>
		<tr>
			<td>2</td>
			<td>Enter</td>
			<td>1</td>
			<td>1</td>
		</tr>
		<tr>
			<td>3</td>
			<td>Leave</td>
			<td>0</td>
			<td>2</td>
		</tr>
		<tr>
			<td>4</td>
			<td>Enter</td>
			<td>1</td>
			<td>1</td>
		</tr>
		<tr>
			<td>5</td>
			<td>Enter</td>
			<td>2</td>
			<td>0</td>
		</tr>
		<tr>
			<td>6</td>
			<td>Leave</td>
			<td>1</td>
			<td>1</td>
		</tr>
	</tbody>
</table>

<p><strong class="example">Example 3:</strong></p>

<div class="example-block">
<p><strong>Input:</strong> <span class="example-io">s = &quot;ELEELEELLL&quot;</span></p>

<p><strong>Output:</strong> <span class="example-io">3</span></p>

<p><strong>Explanation:</strong></p>

<p>Let&#39;s consider that there are 3 chairs in the waiting room. The table below shows the state of the waiting room at each second.</p>
</div>

<table>
	<tbody>
		<tr>
			<th>Second</th>
			<th>Event</th>
			<th>People in the Waiting Room</th>
			<th>Available Chairs</th>
		</tr>
		<tr>
			<td>0</td>
			<td>Enter</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr>
			<td>1</td>
			<td>Leave</td>
			<td>0</td>
			<td>3</td>
		</tr>
		<tr>
			<td>2</td>
			<td>Enter</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr>
			<td>3</td>
			<td>Enter</td>
			<td>2</td>
			<td>1</td>
		</tr>
		<tr>
			<td>4</td>
			<td>Leave</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr>
			<td>5</td>
			<td>Enter</td>
			<td>2</td>
			<td>1</td>
		</tr>
		<tr>
			<td>6</td>
			<td>Enter</td>
			<td>3</td>
			<td>0</td>
		</tr>
		<tr>
			<td>7</td>
			<td>Leave</td>
			<td>2</td>
			<td>1</td>
		</tr>
		<tr>
			<td>8</td>
			<td>Leave</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr>
			<td>9</td>
			<td>Leave</td>
			<td>0</td>
			<td>3</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= s.length &lt;= 50</code></li>
	<li><code>s</code> consists only of the letters <code>&#39;E&#39;</code> and <code>&#39;L&#39;</code>.</li>
	<li><code>s</code> represents a valid sequence of entries and exits.</li>
</ul>


<P>🧠 𝐀𝐩𝐩𝐫𝐨𝐚𝐜𝐡 𝐚𝐧𝐝 𝐒𝐨𝐥𝐮𝐭𝐢𝐨𝐧: <br>
◾ In this solution, we maintain 𝐭𝐰𝐨 𝐯𝐚𝐫𝐢𝐚𝐛𝐥𝐞𝐬: <br>
--> 𝐩𝐞𝐫𝐬𝐨𝐧: to track the number of people currently in the waiting room. <br>
--> 𝐜𝐡𝐚𝐢𝐫𝐬: to keep track of the number of chairs needed. <br>
◾ For each character in the string: <br>
--> If it's '𝐄', a person enters, so we 𝐢𝐧𝐜𝐫𝐞𝐦𝐞𝐧𝐭 person. If the number of people exceeds the number of chairs, we 𝐚𝐝𝐝 a chair. <br>
--> If it's '𝐋', a person leaves, so we 𝐝𝐞𝐜𝐫𝐞𝐦𝐞𝐧𝐭 person. <br>
This simple yet efficient approach ensures to simulate the chair requirements over time. <br>
 <hr>
⏳ 𝗖𝗼𝗺𝗽𝗹𝗲𝘅𝗶𝘁𝘆 𝗔𝗻𝗮𝗹𝘆𝘀𝗶𝘀: <br>
-> 𝗧𝗶𝗺𝗲 𝗖𝗼𝗺𝗽𝗹𝗲𝘅𝗶𝘁𝘆: O(N) <br>
As we iterate through the string 𝐬 once, making this solution 𝐥𝐢𝐧𝐞𝐚𝐫 in time complexity. <br>
-> 𝗦𝗽𝗮𝗰𝗲 𝗖𝗼𝗺𝗽𝗹𝗲𝘅𝗶𝘁𝘆: O(1) <br>
The solution uses a 𝐜𝐨𝐧𝐬𝐭𝐚𝐧𝐭 amount of space.  <br> <p>
