**Room Link**: [https://tryhackme.com/room/linuxcli-aoc2025-o1fpqkvxti](https://tryhackme.com/room/linuxcli-aoc2025-o1fpqkvxti)

## ▶️ Ryan Montgomery – Day 1 Video Walkthrough  
We are providing the official Day 1 walkthrough video for quick onboarding:

🔗 **YouTube Link:** [https://youtu.be/enOqvR0-1O4?si=ICiOoy59nfKVHCki](https://youtu.be/enOqvR0-1O4?si=ICiOoy59nfKVHCki)

<br>


<h1>🐧 Advent of Cyber — Day 1 Write-Up </h1>

<h2>Question 1 — Which CLI command lists the contents of a directory?</h2>
<p>When you enter McSkidy’s home directory, the first step is checking what’s available.</p>
<H3>Answer: </H3>
<h3><pre><code>ls</code></pre></h3>

<img width="1336" height="60" alt="ls" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day1/Q1_ls.png?raw=true" />

<!-- <p>This reveals directories, files, and symlinks, including the <strong>Guides</strong> directory.</p> -->

<hr />

<h2>Question 2 — What flag was hidden inside McSkidy’s guide?</h2>

<p>Navigate into the Guides directory:</p>

<pre><code>cd Guides</code></pre>

<p>The folder looks empty until you reveal hidden files:</p>

<pre><code>ls -la</code></pre>

<p>Which exposes .guide.txt</p>

<pre><code>cat .guide.txt</code></pre>

<img width="1246" height="553" alt="flag1" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day1/Q2_flag1.png?raw=true" />
<H3>Answer: </H3>
<h3><pre><code>THM{learning-linux-cli}</code></pre></h3>

<hr />

<h2>Question 3 — Which command filtered failed login attempts?</h2>

<pre><code>cd /var/log</code></pre>
<pre><code>grep "Failed password" auth.log</code></pre>

<img width="1907" height="792" alt="greplogs" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day1/Q3_greplogs.png?raw=true" />

<H3>Answer: </H3>
<h3><pre><code>grep</code></pre></h3>


<hr />

<h2>Question 4 — What flag was inside the Eggstrike script?</h2>

<p>Search the socmas directory:</p>

<pre><code>find /home/socmas -name "*egg*"</code></pre>
<img width="1836" height="329" alt="flag2" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day1/Q4_flag2.png?raw=true" />
<H3>Answer: </H3>
<h3><pre><code>THM{sir-carrotbane-attacks}</code></pre></h3>

<hr />

<h2>Question 5 — Which command switches to the root user?</h2>
<H3>Answer: </H3>
<h3><pre><code>sudo su</code></pre></h3>

<hr />

<h2>Question 6 — What flag was found in root’s bash history?</h2>

<pre><code>cd /root</code></pre>
<pre><code>cat .bash_history</code></pre>
<img width="1891" height="427" alt="flag3" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day1/Q6_flag3.png?raw=true" />
<H3>Answer: </H3>
<h3><pre><code>THM{until-we-meet-again}</code></pre></h3>




<hr />
