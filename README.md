      <div class="Box-body">
        <article class="markdown-body entry-content p-5" itemprop="text"><h2><a id="user-content-introduction" class="anchor" aria-hidden="true" href="#introduction"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Introduction</h2>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/bcec1bc2d0ec70cb400d191a4054be319e24757c/687474703a2f2f342e62702e626c6f6773706f742e636f6d2f2d676250724162374741624d2f55765756775567446d36492f41414141414141414964492f53545061545165727874672f73313630302f666c61742d66696c652d6775657374626f6f6b2d776974682d7068702e706e67"><img src="https://camo.githubusercontent.com/bcec1bc2d0ec70cb400d191a4054be319e24757c/687474703a2f2f342e62702e626c6f6773706f742e636f6d2f2d676250724162374741624d2f55765756775567446d36492f41414141414141414964492f53545061545165727874672f73313630302f666c61742d66696c652d6775657374626f6f6b2d776974682d7068702e706e67" alt="Screenshot" data-canonical-src="http://4.bp.blogspot.com/-gbPrAb7GAbM/UvWVwUgDm6I/AAAAAAAAIdI/STPaTQerxtg/s1600/flat-file-guestbook-with-php.png" style="max-width:100%;"></a></p>
<p><em>Flat-File GuestBook</em> is a simple-single file guestbook application without database written in PHP. Instead, the user data will be stored into a text file.</p>
<h2><a id="user-content-details" class="anchor" aria-hidden="true" href="#details"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Details</h2>
<p>Download and extract the file to get a <code>guestbook</code> folder. Copy the folder and it’s contents then paste to your localhost folder.</p>
<p>Now open <code>http://localhost/guestbook/index.php</code> with your favorite browser. <em>Done!</em></p>
<h2><a id="user-content-configurations" class="anchor" aria-hidden="true" href="#configurations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Configurations</h2>
<div class="highlight highlight-source-hack"><pre><span class="pl-c"><span class="pl-c">//</span> START CONFIGURATION</span>
<span class="pl-smi">$database</span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">'</span>database-001<span class="pl-pds">'</span></span>; <span class="pl-c"><span class="pl-c">//</span> Your TXT file name as database.</span>
<span class="pl-smi">$per_page</span> <span class="pl-k">=</span> <span class="pl-c1">5</span>; <span class="pl-c"><span class="pl-c">//</span> The number of items you want to display per page.</span>
<span class="pl-smi">$time_zone</span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">'</span>Asia/Jakarta<span class="pl-pds">'</span></span>; <span class="pl-c"><span class="pl-c">//</span> Look at `date_default_timezone_set()`</span>
<span class="pl-smi">$max_length_name</span> <span class="pl-k">=</span> <span class="pl-c1">60</span>; <span class="pl-c"><span class="pl-c">//</span> Maximum character length for guest name</span>
<span class="pl-smi">$max_length_url</span> <span class="pl-k">=</span> <span class="pl-c1">120</span>; <span class="pl-c"><span class="pl-c">//</span> Maximum character length for guest URL</span>
<span class="pl-smi">$max_length_message</span> <span class="pl-k">=</span> <span class="pl-c1">1000</span>; <span class="pl-c"><span class="pl-c">//</span> Maximum character length for guest message</span>
<span class="pl-smi">$messages</span> <span class="pl-k">=</span> <span class="pl-c1">array</span>(
    <span class="pl-s"><span class="pl-pds">'</span>database_missing<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Database not found. Created one. Please reload the page.<span class="pl-pds">'</span></span>,
    <span class="pl-s"><span class="pl-pds">'</span>name_missing<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Please enter your name.<span class="pl-pds">'</span></span>,
    <span class="pl-s"><span class="pl-pds">'</span>url_invalid<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Invalid URL.<span class="pl-pds">'</span></span>,
    <span class="pl-s"><span class="pl-pds">'</span>message_missing<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Please enter your message.<span class="pl-pds">'</span></span>,
    <span class="pl-s"><span class="pl-pds">'</span>math_invalid<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Wrong math answer.<span class="pl-pds">'</span></span>,
    <span class="pl-s"><span class="pl-pds">'</span>max_length_name<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Maximum character length for guest name is <span class="pl-pds">'</span></span> <span class="pl-k">.</span> <span class="pl-smi">$max_length_name</span>,
    <span class="pl-s"><span class="pl-pds">'</span>max_length_url<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Maximum character length for guest URL is <span class="pl-pds">'</span></span> <span class="pl-k">.</span> <span class="pl-smi">$max_length_url</span>,
    <span class="pl-s"><span class="pl-pds">'</span>max_length_message<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>Maximum character length for guest message is <span class="pl-pds">'</span></span> <span class="pl-k">.</span> <span class="pl-smi">$max_length_message</span>,
    <span class="pl-s"><span class="pl-pds">'</span>no_content<span class="pl-pds">'</span></span> <span class="pl-k">=&gt;</span> <span class="pl-s"><span class="pl-pds">'</span>No content.<span class="pl-pds">'</span></span>
);
<span class="pl-c"><span class="pl-c">//</span> END CONFIGURATION</span></pre></div>
</article>
