<h1>browser_analysis</h1>
<p>
1.Firstly , the scheme for the neverssl website is http where as for the github and youtube ones it’s https. Secondly neverssl has no security or authority policies . whereas such policies exist for github in the form of cookies and similarly for youtube a permission policy is present.Also the youtube and github has things like strict transport policy, content security policy which is absent in the neverssl one. Also when you open the nerssl page you always see a danger sign showing the website isn’t safe, but that isn’t the case in the github and youtube ones there you clearly see a lock which indicates the security of the page.

</br>

HTTP: Yes — request headers and bodies are sent in plaintext; so anyone using the network  can read them.</br>
HTTPS: No — the request is encrypted on the wire by TLS(transport level security, basically encrypts all the data that travels between our browser and the web server. ). DevTools shows you the decrypted content because the browser decrypts it; an external passive attacker cannot.

</br>

These are the reasons why https is better than http</br>
It provides confidentiality through encryption.</br>
Maintains integrity by tamper detection.</br>
It also authenticates the server identity via certificates.</br>



2. For neverssl u get 3 requests. </br>
    For github u get 212 requests. </br>
   For youtube it depends on the time of recording for a minute. I got 107 requests.
</br>


For  neverssl (JS -1 , doc -1, other -1)</br>
For github (fetch -11 ,doc -1, css-31, js-149 ,img -8 , manifest -1 , other-18 )</br>
For youtube(fetch-31 ,doc-2, css-8,js-21, font-2, img-27 , media-4, manifest-1, other-10)</br>


Typically youtube will make the most because it loads many image thumbnails, video manifests, player scripts, ad/tracking calls and additional XHRs for recommendations and analytics. GitHub is a complex web app and will also have many JS and API calls. neverssl is intentionally minimal and will have very few requests.

</br>
3.the load time for nverssl is 1.96 secs.</br>
   The load time for github is 2.16 secs</br>
The load time for youtube is 3.77 secs.</br>
The load time is highest for youtube from the stats.</br>



</p>
