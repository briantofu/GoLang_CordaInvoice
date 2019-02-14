---


---

<h2 id="hyperledger-fabric-samples">Hyperledger Fabric Samples</h2>
<p>Please visit the <a href="http://hyperledger-fabric.readthedocs.io/en/latest/install.html">installation instructions</a><br>
to ensure you have the correct prerequisites installed. Please use the<br>
version of the documentation that matches the version of the software you<br>
intend to use to ensure alignment.</p>
<h2 id="download-binaries-and-docker-images">Download Binaries and Docker Images</h2>
<p>The <a href="https://github.com/hyperledger/fabric-samples/blob/release-1.3/scripts/bootstrap.sh"><code>scripts/bootstrap.sh</code></a><br>
script will preload all of the requisite docker<br>
images for Hyperledger Fabric and tag them with the ‘latest’ tag. Optionally,<br>
specify a version for fabric, fabric-ca and thirdparty images. Default versions<br>
are 1.3.0, 1.3.0 and 0.4.13 respectively.</p>
<pre class=" language-bash"><code class="prism  language-bash">./scripts/bootstrap.sh <span class="token punctuation">[</span>version<span class="token punctuation">]</span> <span class="token punctuation">[</span>ca version<span class="token punctuation">]</span> <span class="token punctuation">[</span>thirdparty_version<span class="token punctuation">]</span>
</code></pre>
<h2 id="license-a-namelicensea">License <a></a></h2>
<p>Hyperledger Project source code files are made available under the Apache<br>
License, Version 2.0 (Apache-2.0), located in the <a href="LICENSE">LICENSE</a> file.<br>
Hyperledger Project documentation files are made available under the Creative<br>
Commons Attribution 4.0 International License (CC-BY-4.0), available at <a href="http://creativecommons.org/licenses/by/4.0/">http://creativecommons.org/licenses/by/4.0/</a>.</p>
<h1 id="section"><img src="https://docs.google.com/drawings/d/sYEBgBmeLQ8alj-GCpQbD-g/image?w=68&amp;h=6&amp;rev=1&amp;ac=1&amp;parent=1usGyvQKixUfqVq7u4h-0SX0zNHx0x4Apa7TCErMYuLg" alt=""></h1>
<h1 id="requirements-for-invoice">Requirements for Invoice</h1>
<p>These are the requirements on how to run the Invoice on the Terminal with the Hyperledger Fabric:</p>
<ul>
<li>
<p>GoLang 1.11.5</p>
</li>
<li>
<p>Hyperledger Fabric</p>
</li>
<li>
<p>VS Code 1.30</p>
</li>
<li>
<p>NodeJS</p>
</li>
<li>
<p>Postman</p>
</li>
<li>
<p>VSCode Go Extension</p>
</li>
<li>
<p>Ubuntu 16.04 LTS up</p>
</li>
<li>
<p>Docker Compose</p>
</li>
</ul>
<h1 id="section-1"><img src="https://docs.google.com/drawings/d/s0O3qNTd-DafwZvIlOqGYYg/image?w=68&amp;h=6&amp;rev=1&amp;ac=1&amp;parent=1usGyvQKixUfqVq7u4h-0SX0zNHx0x4Apa7TCErMYuLg" alt=""></h1>
<h1 id="steps">Steps</h1>
<p>Installing GoLang:</p>
<ol>
<li>
<p>Go to the link: <a href="https://golang.org/">https://golang.org/</a></p>
</li>
<li>
<p>In the website, click ‘Download Go’</p>
</li>
<li>
<p>There are versions of Golang that will be installed onto the system unit. On my case, I will download the Linux Version on 1.11.5.</p>
</li>
<li>
<p>There are options to extract the contents of the Linux Version of Golang. Extract it onto the home folder, which is your username of your laptop or use the terminal execution by the use of this command when you open the terminal. ‘sudo snap install go --classic’</p>
</li>
<li>
<p>Export the path so that your extracted files that you’ve installed with it. Exceute on this terminal</p>
</li>
</ol>
<p>export GOROOT=/usr/local/go</p>
<p>export GOPATH=$HOME/go</p>
<p>export PATH=<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>G</mi><mi>O</mi><mi>P</mi><mi>A</mi><mi>T</mi><mi>H</mi><mi mathvariant="normal">/</mi><mi>b</mi><mi>i</mi><mi>n</mi><mo>:</mo></mrow><annotation encoding="application/x-tex">GOPATH/bin:</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord mathit">G</span><span class="mord mathit" style="margin-right: 0.02778em;">O</span><span class="mord mathit" style="margin-right: 0.13889em;">P</span><span class="mord mathit">A</span><span class="mord mathit" style="margin-right: 0.13889em;">T</span><span class="mord mathit" style="margin-right: 0.08125em;">H</span><span class="mord">/</span><span class="mord mathit">b</span><span class="mord mathit">i</span><span class="mord mathit">n</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">:</span></span></span></span></span>GOROOT/bin:$PATH</p>
<p>Installing VSCode:</p>
<ol>
<li>
<p>Go to this link: <a href="https://code.visualstudio.com/">https://code.visualstudio.com/</a> . For my case, I downloaded the .deb file which supports Ubuntu.</p>
</li>
<li>
<p>Just run it through the use of installation manager and automatically when you search on the dashboard, you will see the VSCode.</p>
</li>
</ol>
<p>Installing Insomia:</p>
<p>Add to sources</p>
<p>echo “deb <a href="https://dl.bintray.com/getinsomnia/Insomnia">https://dl.bintray.com/getinsomnia/Insomnia</a> /” \<br>
| sudo tee -a /etc/apt/sources.list.d/insomnia.list</p>
<p>Add public key used to verify code signature</p>
<p>wget --quiet -O - <a href="https://insomnia.rest/keys/debian-public.key.asc">https://insomnia.rest/keys/debian-public.key.asc</a> \<br>
| sudo apt-key add -</p>
<p>Refresh repository sources and install Insomnia</p>
<p>sudo apt-get update<br>
sudo apt-get install insomnia</p>
<h1 id="section-2"><img src="https://docs.google.com/drawings/d/sO6W8pmt8doZ2UK7BCorW-w/image?w=68&amp;h=6&amp;rev=1&amp;ac=1&amp;parent=1usGyvQKixUfqVq7u4h-0SX0zNHx0x4Apa7TCErMYuLg" alt=""></h1>
<h1 id="running-the-invoice-application-to-your-machine">Running the Invoice application to your machine</h1>
<ol>
<li>
<p>You should clone the repository folders from github as a tool for running the invoice. From here you must clone using the terminal. Click the ‘clone or download’ button and on the terminal, you can choose what directory by using “cd ‘name of the folder’” and/or create a folder by using “mkdir ‘name of the folder’ and go to the directory on it. You can also do it on the file manager normally.</p>
</li>
<li>
<p>You must clone also the ‘fabric-samples’ link which is on this link. <a href="https://github.com/hyperledger/fabric-samples.git">https://github.com/hyperledger/fabric-samples.git</a>. You must do this also on the terminal.</p>
</li>
<li>
<p>From the fabric-samples folder, you must create a new folder which is invoice. You must do it inside the ‘fabric-samples’ folder that named ‘Invoice’ and also the chaincode folder ‘chaincode --&gt; go --&gt; invoice’.</p>
</li>
<li>
<p>For the folder that you clone from my repository, we have the chaincode folder which it has the file named ‘invoice.go’. Just copy the file and paste it on ‘fabric-samples -&gt; chaincode -&gt; go -&gt; invoice. Also we have the invoice folder on my repository that the content are 4 js files and <a href="http://startFabric.sh">startFabric.sh</a>. Copy also the files and paste in onto this directory. ‘Fabric-samples -&gt; invoice’</p>
</li>
<li>
<p>Open your terminal on the invoice folder inside the ‘fabric-samples’. To provide the fastest way, right click it and click the ‘Open Terminal’</p>
</li>
<li>
<p>Start the fabric server client. On the terminal, just to make sure if the files on there, execute ‘ls’ or the list of files and folder inside. To start, use the ‘./startFabric.sh’.</p>
</li>
<li>
<p>Wait for it and if it is successful, run the enrollAdmin.js by using ‘node enrollAdmin.js’. It will generate a folder named “hfc-key-store’ which stores all of the public and private keys. After that, run also the ‘node registerUser.js’. It will show all of the 3 users; the supplier (IBM), the Lotus (OEM), and the Bank (UBP)</p>
</li>
<li>
<p>Finally, you will execute the ‘node app.js’ which it will run on the localhost:3000. For the API that will be using for execution, I’ve used Insomnia. This applications executes the API of every function that will input and output as a json format.</p>
</li>
<li>
<p>First, open the Insomnia and create a workspace for the invoice. Then create a api function, for this we will first use get all the invoice. If you check the code of invoice.go, we have the function which is initLedger. That function serves as the first data that will be shown on the Insomia.</p>
</li>
<li>
<p>Create it on insomnia by naming a specific function sentence and use ‘GET’ tab. Second, type in the textbox field which is the ‘localhost:3000’ which the ‘3000’ is the port number of the server. Take note that you must put on the ‘Form URL Encoded’. Inside the field is enter your data values which is “usename” and the value must be IBM/ Lotus/UBP.</p>
</li>
<li>
<p>Click send and it will show the arrays of data that fetched on the right side.</p>
</li>
<li>
<p>Create an API function that will insert records. Go to a new api function by clicking the ‘+’ button and click New Request. Name it ‘Insert Invoice’ and go to the ‘GET’ dropdown and use ‘POST’ .</p>
</li>
<li>
<p>On the ‘Body’ tab, click it to show the items and use ‘Form URL Encoded’. Enter this fields:</p>
</li>
</ol>
<ul>
<li>
<p>Username &nbsp;&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;			IBM</p>
</li>
<li>
<p>Invoiceid 		&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;		    INVOICE1</p>
</li>
<li>
<p>Invoicenum  &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;				   1</p>
</li>
<li>
<p>Billed to&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	  (any name)</p>
</li>
<li>
<p>Invoicedate  &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	2/14/2019</p>
</li>
<li>
<p>Invoiceamount &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	 0</p>
</li>
<li>
<p>itemdescription &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	any description</p>
</li>
<li>
<p>Gr &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	 false</p>
</li>
<li>
<p>ispaid &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	false</p>
</li>
<li>
<p>paidamount &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	 0</p>
</li>
<li>
<p>repaid &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	false</p>
</li>
<li>
<p>Repaymentamount  &nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;	0</p>
</li>
</ul>
<p>Enter the address on the url field as ‘localhost:3000/invoice’ and execute the API.</p>
<p>Take note that when you enter mutiple fields, the invoiceid is incremented by 1.</p>
<ol start="14">
<li>
<p>Get History, means the transactions that you entered with the hash transaction number and the timestamp, the date and time of the specific transaction. Just go to new request and name it ‘Get Audit History’ and use Get.</p>
</li>
<li>
<p>On get history, click on the query tab and type the field and input “invoiceid = . And it will show the transaction happened.</p>
</li>
<li>
<p>Another function request is the Suppler to Bank, name it ‘Supplier to Bank’, ‘PUT’ function. The fields are ‘username, invoiceid and paidamount’.</p>
</li>
<li>
<p>For repayment, it is also the same fields and API as ‘PUT’ as the Supplier to Bank.<br>
The difference is instead of paidamount, use repaymentamount.</p>
</li>
</ol>

