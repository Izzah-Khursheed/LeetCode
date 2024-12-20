<p>🧠 𝐀𝐩𝐩𝐫𝐨𝐚𝐜𝐡: <br> 
--> The solution to the problem uses the "𝐃𝐮𝐭𝐜𝐡 𝐍𝐚𝐭𝐢𝐨𝐧𝐚𝐥 𝐅𝐥𝐚𝐠 𝐚𝐥𝐠𝐨𝐫𝐢𝐭𝐡𝐦", 𝐚 𝐭𝐰𝐨-𝐩𝐨𝐢𝐧𝐭𝐞𝐫 𝐭𝐞𝐜𝐡𝐧𝐢𝐪𝐮𝐞 𝐭𝐡𝐚𝐭 𝐞𝐟𝐟𝐢𝐜𝐢𝐞𝐧𝐭𝐥𝐲 <br>
𝐬𝐨𝐫𝐭𝐬 𝐭𝐡𝐞 𝐚𝐫𝐫𝐚𝐲 𝐢𝐧 𝐨𝐧𝐞 𝐩𝐚𝐬𝐬.  <br>
--> The approach involves maintaining 𝐭𝐡𝐫𝐞𝐞 𝐩𝐨𝐢𝐧𝐭𝐞𝐫𝐬: '𝒍𝒐𝒘', '𝒎𝒊𝒅', and '𝒉𝒊𝒈𝒉'. The '𝒍𝒐𝒘' pointer tracks the <br>
position of the last sorted red (0), '𝒎𝒊𝒅' scans through each element, and '𝒉𝒊𝒈𝒉' marks the boundary for blue (2) <br>
elements.<br>
--> Starting from the beginning, '𝒎𝒊𝒅' iterates through the array. If '𝒏𝒖𝒎𝒔[𝒎𝒊𝒅]' 𝒊𝒔 '0', it swaps with <br>
'𝒏𝒖𝒎𝒔[𝒍𝒐𝒘]', increments both '𝒍𝒐𝒘' and '𝒎𝒊𝒅', positioning red elements at the start.<br>
--> If '𝒏𝒖𝒎𝒔[𝒎𝒊𝒅]' 𝒊𝒔 '1', it simply increments '𝒎𝒊𝒅', as whites (1s) stay in the middle.<br>
--> If '𝒏𝒖𝒎𝒔[𝒎𝒊𝒅]' 𝒊𝒔 '2', it swaps with '𝒏𝒖𝒎𝒔[𝒉𝒊𝒈𝒉]' and decrements '𝒉𝒊𝒈𝒉', keeping blues (2s) at the end.<br>
--> This 𝒊𝒏-𝒑𝒍𝒂𝒄𝒆 𝒕𝒆𝒄𝒉𝒏𝒊𝒒𝒖𝒆 achieves the desired order of colors in a single linear pass, making it both <br>
𝒕𝒊𝒎𝒆-𝒆𝒇𝒇𝒊𝒄𝒊𝒆𝒏𝒕 and 𝒎𝒆𝒎𝒐𝒓𝒚-𝒆𝒇𝒇𝒊𝒄𝒊𝒆𝒏𝒕.<br> <br>

⏳ 𝗖𝗼𝗺𝗽𝗹𝗲𝘅𝗶𝘁𝘆 𝗔𝗻𝗮𝗹𝘆𝘀𝗶𝘀:<br>
-> 𝑻𝒊𝒎𝒆 𝑪𝒐𝒎𝒑𝒍𝒆𝒙𝒊𝒕𝒚: O(N)<br>
-> 𝑺𝒑𝒂𝒄𝒆 𝑪𝒐𝒎𝒑𝒍𝒆𝒙𝒊𝒕𝒚: O(1)<br>
</p>
