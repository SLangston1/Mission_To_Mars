

```python
# Dependencies
from bs4 import BeautifulSoup
import requests
from splinter import Browser

import pandas as pd
```


```python
#Scrape NASA Mars News Site
# URL of page to be scraped
url = 'https://mars.nasa.gov/news/'
```


```python
# Retrieve page with the requests module
response = requests.get(url)
```


```python
# Create BeautifulSoup object; parse with 'html.parser'
soup = BeautifulSoup(response.text, 'html.parser')
```


```python
# Examine the results, then determine element that contains sought info
print(soup.prettify())
```

    <!DOCTYPE html>
    <html lang="en" xml:lang="en" xmlns="http://www.w3.org/1999/xhtml">
     <head>
      <meta content="text/html; charset=utf-8" http-equiv="Content-Type"/>
      <!-- Always force latest IE rendering engine or request Chrome Frame -->
      <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
      <script type="text/javascript">
       window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","errorBeacon":"bam.nr-data.net","licenseKey":"5e33925808","applicationID":"59562082","transactionName":"JVcPR0MLWApSRU1eAQVVEhxSC1oSUlkWbBMHXwRAHhdcCUA=","queueTime":0,"applicationTime":155,"agent":""}
      </script>
      <script type="text/javascript">
       (window.NREUM||(NREUM={})).loader_config={xpid:"VQcPUlZTDxAFXVRUBQEPVA=="};window.NREUM||(NREUM={}),__nr_require=function(t,n,e){function r(e){if(!n[e]){var o=n[e]={exports:{}};t[e][0].call(o.exports,function(n){var o=t[e][1][n];return r(o||n)},o,o.exports)}return n[e].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<e.length;o++)r(e[o]);return r}({1:[function(t,n,e){function r(t){try{s.console&&console.log(t)}catch(n){}}var o,i=t("ee"),a=t(15),s={};try{o=localStorage.getItem("__nr_flags").split(","),console&&"function"==typeof console.log&&(s.console=!0,o.indexOf("dev")!==-1&&(s.dev=!0),o.indexOf("nr_dev")!==-1&&(s.nrDev=!0))}catch(c){}s.nrDev&&i.on("internal-error",function(t){r(t.stack)}),s.dev&&i.on("fn-err",function(t,n,e){r(e.stack)}),s.dev&&(r("NR AGENT IN DEVELOPMENT MODE"),r("flags: "+a(s,function(t,n){return t}).join(", ")))},{}],2:[function(t,n,e){function r(t,n,e,r,s){try{p?p-=1:o(s||new UncaughtException(t,n,e),!0)}catch(f){try{i("ierr",[f,c.now(),!0])}catch(d){}}return"function"==typeof u&&u.apply(this,a(arguments))}function UncaughtException(t,n,e){this.message=t||"Uncaught error with no additional information",this.sourceURL=n,this.line=e}function o(t,n){var e=n?null:c.now();i("err",[t,e])}var i=t("handle"),a=t(16),s=t("ee"),c=t("loader"),f=t("gos"),u=window.onerror,d=!1,l="nr@seenError",p=0;c.features.err=!0,t(1),window.onerror=r;try{throw new Error}catch(h){"stack"in h&&(t(8),t(7),"addEventListener"in window&&t(5),c.xhrWrappable&&t(9),d=!0)}s.on("fn-start",function(t,n,e){d&&(p+=1)}),s.on("fn-err",function(t,n,e){d&&!e[l]&&(f(e,l,function(){return!0}),this.thrown=!0,o(e))}),s.on("fn-end",function(){d&&!this.thrown&&p>0&&(p-=1)}),s.on("internal-error",function(t){i("ierr",[t,c.now(),!0])})},{}],3:[function(t,n,e){t("loader").features.ins=!0},{}],4:[function(t,n,e){function r(t){}if(window.performance&&window.performance.timing&&window.performance.getEntriesByType){var o=t("ee"),i=t("handle"),a=t(8),s=t(7),c="learResourceTimings",f="addEventListener",u="resourcetimingbufferfull",d="bstResource",l="resource",p="-start",h="-end",m="fn"+p,w="fn"+h,v="bstTimer",y="pushState",g=t("loader");g.features.stn=!0,t(6);var b=NREUM.o.EV;o.on(m,function(t,n){var e=t[0];e instanceof b&&(this.bstStart=g.now())}),o.on(w,function(t,n){var e=t[0];e instanceof b&&i("bst",[e,n,this.bstStart,g.now()])}),a.on(m,function(t,n,e){this.bstStart=g.now(),this.bstType=e}),a.on(w,function(t,n){i(v,[n,this.bstStart,g.now(),this.bstType])}),s.on(m,function(){this.bstStart=g.now()}),s.on(w,function(t,n){i(v,[n,this.bstStart,g.now(),"requestAnimationFrame"])}),o.on(y+p,function(t){this.time=g.now(),this.startPath=location.pathname+location.hash}),o.on(y+h,function(t){i("bstHist",[location.pathname+location.hash,this.startPath,this.time])}),f in window.performance&&(window.performance["c"+c]?window.performance[f](u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["c"+c]()},!1):window.performance[f]("webkit"+u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["webkitC"+c]()},!1)),document[f]("scroll",r,{passive:!0}),document[f]("keypress",r,!1),document[f]("click",r,!1)}},{}],5:[function(t,n,e){function r(t){for(var n=t;n&&!n.hasOwnProperty(u);)n=Object.getPrototypeOf(n);n&&o(n)}function o(t){s.inPlace(t,[u,d],"-",i)}function i(t,n){return t[1]}var a=t("ee").get("events"),s=t(18)(a,!0),c=t("gos"),f=XMLHttpRequest,u="addEventListener",d="removeEventListener";n.exports=a,"getPrototypeOf"in Object?(r(document),r(window),r(f.prototype)):f.prototype.hasOwnProperty(u)&&(o(window),o(f.prototype)),a.on(u+"-start",function(t,n){var e=t[1],r=c(e,"nr@wrapped",function(){function t(){if("function"==typeof e.handleEvent)return e.handleEvent.apply(e,arguments)}var n={object:t,"function":e}[typeof e];return n?s(n,"fn-",null,n.name||"anonymous"):e});this.wrapped=t[1]=r}),a.on(d+"-start",function(t){t[1]=this.wrapped||t[1]})},{}],6:[function(t,n,e){var r=t("ee").get("history"),o=t(18)(r);n.exports=r,o.inPlace(window.history,["pushState","replaceState"],"-")},{}],7:[function(t,n,e){var r=t("ee").get("raf"),o=t(18)(r),i="equestAnimationFrame";n.exports=r,o.inPlace(window,["r"+i,"mozR"+i,"webkitR"+i,"msR"+i],"raf-"),r.on("raf-start",function(t){t[0]=o(t[0],"fn-")})},{}],8:[function(t,n,e){function r(t,n,e){t[0]=a(t[0],"fn-",null,e)}function o(t,n,e){this.method=e,this.timerDuration=isNaN(t[1])?0:+t[1],t[0]=a(t[0],"fn-",this,e)}var i=t("ee").get("timer"),a=t(18)(i),s="setTimeout",c="setInterval",f="clearTimeout",u="-start",d="-";n.exports=i,a.inPlace(window,[s,"setImmediate"],s+d),a.inPlace(window,[c],c+d),a.inPlace(window,[f,"clearImmediate"],f+d),i.on(c+u,r),i.on(s+u,o)},{}],9:[function(t,n,e){function r(t,n){d.inPlace(n,["onreadystatechange"],"fn-",s)}function o(){var t=this,n=u.context(t);t.readyState>3&&!n.resolved&&(n.resolved=!0,u.emit("xhr-resolved",[],t)),d.inPlace(t,y,"fn-",s)}function i(t){g.push(t),h&&(x?x.then(a):w?w(a):(E=-E,O.data=E))}function a(){for(var t=0;t<g.length;t++)r([],g[t]);g.length&&(g=[])}function s(t,n){return n}function c(t,n){for(var e in t)n[e]=t[e];return n}t(5);var f=t("ee"),u=f.get("xhr"),d=t(18)(u),l=NREUM.o,p=l.XHR,h=l.MO,m=l.PR,w=l.SI,v="readystatechange",y=["onload","onerror","onabort","onloadstart","onloadend","onprogress","ontimeout"],g=[];n.exports=u;var b=window.XMLHttpRequest=function(t){var n=new p(t);try{u.emit("new-xhr",[n],n),n.addEventListener(v,o,!1)}catch(e){try{u.emit("internal-error",[e])}catch(r){}}return n};if(c(p,b),b.prototype=p.prototype,d.inPlace(b.prototype,["open","send"],"-xhr-",s),u.on("send-xhr-start",function(t,n){r(t,n),i(n)}),u.on("open-xhr-start",r),h){var x=m&&m.resolve();if(!w&&!m){var E=1,O=document.createTextNode(E);new h(a).observe(O,{characterData:!0})}}else f.on("fn-end",function(t){t[0]&&t[0].type===v||a()})},{}],10:[function(t,n,e){function r(t){var n=this.params,e=this.metrics;if(!this.ended){this.ended=!0;for(var r=0;r<d;r++)t.removeEventListener(u[r],this.listener,!1);if(!n.aborted){if(e.duration=a.now()-this.startTime,4===t.readyState){n.status=t.status;var i=o(t,this.lastSize);if(i&&(e.rxSize=i),this.sameOrigin){var c=t.getResponseHeader("X-NewRelic-App-Data");c&&(n.cat=c.split(", ").pop())}}else n.status=0;e.cbTime=this.cbTime,f.emit("xhr-done",[t],t),s("xhr",[n,e,this.startTime])}}}function o(t,n){var e=t.responseType;if("json"===e&&null!==n)return n;var r="arraybuffer"===e||"blob"===e||"json"===e?t.response:t.responseText;return h(r)}function i(t,n){var e=c(n),r=t.params;r.host=e.hostname+":"+e.port,r.pathname=e.pathname,t.sameOrigin=e.sameOrigin}var a=t("loader");if(a.xhrWrappable){var s=t("handle"),c=t(11),f=t("ee"),u=["load","error","abort","timeout"],d=u.length,l=t("id"),p=t(14),h=t(13),m=window.XMLHttpRequest;a.features.xhr=!0,t(9),f.on("new-xhr",function(t){var n=this;n.totalCbs=0,n.called=0,n.cbTime=0,n.end=r,n.ended=!1,n.xhrGuids={},n.lastSize=null,p&&(p>34||p<10)||window.opera||t.addEventListener("progress",function(t){n.lastSize=t.loaded},!1)}),f.on("open-xhr-start",function(t){this.params={method:t[0]},i(this,t[1]),this.metrics={}}),f.on("open-xhr-end",function(t,n){"loader_config"in NREUM&&"xpid"in NREUM.loader_config&&this.sameOrigin&&n.setRequestHeader("X-NewRelic-ID",NREUM.loader_config.xpid)}),f.on("send-xhr-start",function(t,n){var e=this.metrics,r=t[0],o=this;if(e&&r){var i=h(r);i&&(e.txSize=i)}this.startTime=a.now(),this.listener=function(t){try{"abort"===t.type&&(o.params.aborted=!0),("load"!==t.type||o.called===o.totalCbs&&(o.onloadCalled||"function"!=typeof n.onload))&&o.end(n)}catch(e){try{f.emit("internal-error",[e])}catch(r){}}};for(var s=0;s<d;s++)n.addEventListener(u[s],this.listener,!1)}),f.on("xhr-cb-time",function(t,n,e){this.cbTime+=t,n?this.onloadCalled=!0:this.called+=1,this.called!==this.totalCbs||!this.onloadCalled&&"function"==typeof e.onload||this.end(e)}),f.on("xhr-load-added",function(t,n){var e=""+l(t)+!!n;this.xhrGuids&&!this.xhrGuids[e]&&(this.xhrGuids[e]=!0,this.totalCbs+=1)}),f.on("xhr-load-removed",function(t,n){var e=""+l(t)+!!n;this.xhrGuids&&this.xhrGuids[e]&&(delete this.xhrGuids[e],this.totalCbs-=1)}),f.on("addEventListener-end",function(t,n){n instanceof m&&"load"===t[0]&&f.emit("xhr-load-added",[t[1],t[2]],n)}),f.on("removeEventListener-end",function(t,n){n instanceof m&&"load"===t[0]&&f.emit("xhr-load-removed",[t[1],t[2]],n)}),f.on("fn-start",function(t,n,e){n instanceof m&&("onload"===e&&(this.onload=!0),("load"===(t[0]&&t[0].type)||this.onload)&&(this.xhrCbStart=a.now()))}),f.on("fn-end",function(t,n){this.xhrCbStart&&f.emit("xhr-cb-time",[a.now()-this.xhrCbStart,this.onload,n],n)})}},{}],11:[function(t,n,e){n.exports=function(t){var n=document.createElement("a"),e=window.location,r={};n.href=t,r.port=n.port;var o=n.href.split("://");!r.port&&o[1]&&(r.port=o[1].split("/")[0].split("@").pop().split(":")[1]),r.port&&"0"!==r.port||(r.port="https"===o[0]?"443":"80"),r.hostname=n.hostname||e.hostname,r.pathname=n.pathname,r.protocol=o[0],"/"!==r.pathname.charAt(0)&&(r.pathname="/"+r.pathname);var i=!n.protocol||":"===n.protocol||n.protocol===e.protocol,a=n.hostname===document.domain&&n.port===e.port;return r.sameOrigin=i&&(!n.hostname||a),r}},{}],12:[function(t,n,e){function r(){}function o(t,n,e){return function(){return i(t,[f.now()].concat(s(arguments)),n?null:this,e),n?void 0:this}}var i=t("handle"),a=t(15),s=t(16),c=t("ee").get("tracer"),f=t("loader"),u=NREUM;"undefined"==typeof window.newrelic&&(newrelic=u);var d=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",p=l+"ixn-";a(d,function(t,n){u[n]=o(l+n,!0,"api")}),u.addPageAction=o(l+"addPageAction",!0),u.setCurrentRouteName=o(l+"routeName",!0),n.exports=newrelic,u.interaction=function(){return(new r).get()};var h=r.prototype={createTracer:function(t,n){var e={},r=this,o="function"==typeof n;return i(p+"tracer",[f.now(),t,e],r),function(){if(c.emit((o?"":"no-")+"fn-start",[f.now(),r,o],e),o)try{return n.apply(this,arguments)}catch(t){throw c.emit("fn-err",[arguments,this,t],e),t}finally{c.emit("fn-end",[f.now()],e)}}}};a("setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(t,n){h[n]=o(p+n)}),newrelic.noticeError=function(t){"string"==typeof t&&(t=new Error(t)),i("err",[t,f.now()])}},{}],13:[function(t,n,e){n.exports=function(t){if("string"==typeof t&&t.length)return t.length;if("object"==typeof t){if("undefined"!=typeof ArrayBuffer&&t instanceof ArrayBuffer&&t.byteLength)return t.byteLength;if("undefined"!=typeof Blob&&t instanceof Blob&&t.size)return t.size;if(!("undefined"!=typeof FormData&&t instanceof FormData))try{return JSON.stringify(t).length}catch(n){return}}}},{}],14:[function(t,n,e){var r=0,o=navigator.userAgent.match(/Firefox[\/\s](\d+\.\d+)/);o&&(r=+o[1]),n.exports=r},{}],15:[function(t,n,e){function r(t,n){var e=[],r="",i=0;for(r in t)o.call(t,r)&&(e[i]=n(r,t[r]),i+=1);return e}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],16:[function(t,n,e){function r(t,n,e){n||(n=0),"undefined"==typeof e&&(e=t?t.length:0);for(var r=-1,o=e-n||0,i=Array(o<0?0:o);++r<o;)i[r]=t[n+r];return i}n.exports=r},{}],17:[function(t,n,e){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],18:[function(t,n,e){function r(t){return!(t&&t instanceof Function&&t.apply&&!t[a])}var o=t("ee"),i=t(16),a="nr@original",s=Object.prototype.hasOwnProperty,c=!1;n.exports=function(t,n){function e(t,n,e,o){function nrWrapper(){var r,a,s,c;try{a=this,r=i(arguments),s="function"==typeof e?e(r,a):e||{}}catch(f){l([f,"",[r,a,o],s])}u(n+"start",[r,a,o],s);try{return c=t.apply(a,r)}catch(d){throw u(n+"err",[r,a,d],s),d}finally{u(n+"end",[r,a,c],s)}}return r(t)?t:(n||(n=""),nrWrapper[a]=t,d(t,nrWrapper),nrWrapper)}function f(t,n,o,i){o||(o="");var a,s,c,f="-"===o.charAt(0);for(c=0;c<n.length;c++)s=n[c],a=t[s],r(a)||(t[s]=e(a,f?s+o:o,i,s))}function u(e,r,o){if(!c||n){var i=c;c=!0;try{t.emit(e,r,o,n)}catch(a){l([a,e,r,o])}c=i}}function d(t,n){if(Object.defineProperty&&Object.keys)try{var e=Object.keys(t);return e.forEach(function(e){Object.defineProperty(n,e,{get:function(){return t[e]},set:function(n){return t[e]=n,n}})}),n}catch(r){l([r])}for(var o in t)s.call(t,o)&&(n[o]=t[o]);return n}function l(n){try{t.emit("internal-error",n)}catch(e){}}return t||(t=o),e.inPlace=f,e.flag=a,e}},{}],ee:[function(t,n,e){function r(){}function o(t){function n(t){return t&&t instanceof r?t:t?c(t,s,i):i()}function e(e,r,o,i){if(!l.aborted||i){t&&t(e,r,o);for(var a=n(o),s=h(e),c=s.length,f=0;f<c;f++)s[f].apply(a,r);var d=u[y[e]];return d&&d.push([g,e,r,a]),a}}function p(t,n){v[t]=h(t).concat(n)}function h(t){return v[t]||[]}function m(t){return d[t]=d[t]||o(e)}function w(t,n){f(t,function(t,e){n=n||"feature",y[e]=n,n in u||(u[n]=[])})}var v={},y={},g={on:p,emit:e,get:m,listeners:h,context:n,buffer:w,abort:a,aborted:!1};return g}function i(){return new r}function a(){(u.api||u.feature)&&(l.aborted=!0,u=l.backlog={})}var s="nr@context",c=t("gos"),f=t(15),u={},d={},l=n.exports=o();l.backlog=u},{}],gos:[function(t,n,e){function r(t,n,e){if(o.call(t,n))return t[n];var r=e();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(t,n,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return t[n]=r,r}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(t,n,e){function r(t,n,e,r){o.buffer([t],r),o.emit(t,n,e)}var o=t("ee").get("handle");n.exports=r,r.ee=o},{}],id:[function(t,n,e){function r(t){var n=typeof t;return!t||"object"!==n&&"function"!==n?-1:t===window?0:a(t,i,function(){return o++})}var o=1,i="nr@id",a=t("gos");n.exports=r},{}],loader:[function(t,n,e){function r(){if(!x++){var t=b.info=NREUM.info,n=l.getElementsByTagName("script")[0];if(setTimeout(u.abort,3e4),!(t&&t.licenseKey&&t.applicationID&&n))return u.abort();f(y,function(n,e){t[n]||(t[n]=e)}),c("mark",["onload",a()+b.offset],null,"api");var e=l.createElement("script");e.src="https://"+t.agent,n.parentNode.insertBefore(e,n)}}function o(){"complete"===l.readyState&&i()}function i(){c("mark",["domContent",a()+b.offset],null,"api")}function a(){return E.exists&&performance.now?Math.round(performance.now()):(s=Math.max((new Date).getTime(),s))-b.offset}var s=(new Date).getTime(),c=t("handle"),f=t(15),u=t("ee"),d=window,l=d.document,p="addEventListener",h="attachEvent",m=d.XMLHttpRequest,w=m&&m.prototype;NREUM.o={ST:setTimeout,SI:d.setImmediate,CT:clearTimeout,XHR:m,REQ:d.Request,EV:d.Event,PR:d.Promise,MO:d.MutationObserver};var v=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1071.min.js"},g=m&&w&&w[p]&&!/CriOS/.test(navigator.userAgent),b=n.exports={offset:s,now:a,origin:v,features:{},xhrWrappable:g};t(12),l[p]?(l[p]("DOMContentLoaded",i,!1),d[p]("load",r,!1)):(l[h]("onreadystatechange",o),d[h]("onload",r)),c("mark",["firstbyte",s],null,"api");var x=0,E=t(17)},{}]},{},["loader",2,10,4,3]);
      </script>
      <!-- Responsiveness -->
      <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
      <!-- Favicon -->
      <link href="/apple-touch-icon.png" rel="apple-touch-icon" sizes="180x180"/>
      <link href="/favicon-32x32.png" rel="icon" sizes="32x32" type="image/png"/>
      <link href="/favicon-16x16.png" rel="icon" sizes="16x16" type="image/png"/>
      <link href="/manifest.json" rel="manifest"/>
      <link color="#e48b55" href="/safari-pinned-tab.svg" rel="mask-icon"/>
      <meta content="#000000" name="theme-color"/>
      <meta content="authenticity_token" name="csrf-param">
       <meta content="tefn+zfFNoorkt8tPIBE9jw8cNum+AhokGRsy4kxO5I=" name="csrf-token">
        <title>
         News  – NASA’s Mars Exploration Program
        </title>
        <meta content="NASA’s Mars Exploration Program " property="og:site_name"/>
        <meta content="mars.nasa.gov" name="author"/>
        <meta content="Mars, missions, NASA, rover, Curiosity, Opportunity, InSight, Mars Reconnaissance Orbiter, facts" name="keywords"/>
        <meta content="NASA’s real-time portal for Mars exploration, featuring the latest news, images, and discoveries from the Red Planet." name="description"/>
        <meta content="NASA’s real-time portal for Mars exploration, featuring the latest news, images, and discoveries from the Red Planet." property="og:description"/>
        <meta content="News  – NASA’s Mars Exploration Program " property="og:title"/>
        <meta content="https://mars.nasa.gov/news" property="og:url"/>
        <meta content="article" property="og:type"/>
        <meta content="2017-09-22 19:53:22 UTC" property="og:updated_time"/>
        <meta content="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" property="og:image"/>
        <meta content="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" name="twitter:image"/>
        <link href="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" rel="image_src"/>
        <meta content="195570401081308" property="fb:app_id"/>
        <link href="https://fonts.googleapis.com/css?family=Montserrat:200,300,400,500,600,700|Raleway:300,400" rel="stylesheet"/>
        <link href="/assets/public_manifest-e05f97cdafb31d988d511960c6c62e08ece83d37c15daa3b9b991e2bc176a1e3.css" media="all" rel="stylesheet">
         <link href="/assets/gulp/vendor/jquery.fancybox-364352e03618ba5a8da007665b1f0be31795293b22bc4d7c5974891d4976a137.css" media="screen" rel="stylesheet">
          <link href="/assets/gulp/print-240f8bfaa7f6402dfd6c49ee3c1ffea57a89ddd4c8c90e2f2a5c7d63c5753e32.css" media="print" rel="stylesheet">
           <script src="/assets/public_manifest-7136bdf7a3a8424b034f333778efdc8dd66c789f18847281907defafc52d017e.js">
           </script>
           <!--[if gt IE 8]><!-->
           <script src="/assets/not_ie8_manifest.js">
           </script>
           <!--[if !IE]>-->
           <script src="/assets/not_ie8_manifest.js">
           </script>
           <!--<![endif]-->
           <script src="/assets/vendor/jquery.fancybox-9d361e5f98a5c0f233a25df9252dbadea6897af1c0ef221d7465e1205941ea0d.js">
           </script>
           <script src="/assets/mb_manifest-86cde101f747092d1465039f6da3fd2930c66319387c196503d3f70665195392.js">
           </script>
           <!-- /twitter cards -->
           <meta content="summary_large_image" name="twitter:card"/>
           <meta content="News " name="twitter:title"/>
           <meta content="NASA’s real-time portal for Mars exploration, featuring the latest news, images, and discoveries from the Red Planet." name="twitter:description"/>
           <meta content="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" name="twitter:image"/>
          </link>
         </link>
        </link>
       </meta>
      </meta>
     </head>
     <body id="news">
      <div data-react-class="BrowseHappier" data-react-props='{"gt":1,"lt":11}'>
      </div>
      <div id="main_container">
       <div id="site_body">
        <div class="site_header_area">
         <header class="site_header">
          <div class="brand_area">
           <div class="brand1">
            <a class="nasa_logo" href="http://www.nasa.gov" target="_blank" title="visit nasa.gov">
             NASA
            </a>
           </div>
           <div class="brand2">
            <a class="top_logo" href="https://science.nasa.gov/" target="_blank" title="Explore NASA Science">
             NASA Science
            </a>
            <a class="sub_logo" href="/mars-exploration/#" title="Mars">
             Mars Exploration Program
            </a>
           </div>
           <img alt="" class="print_only print_logo" src="/assets/logo_nasa_trio_black@2x.png"/>
          </div>
          <a class="visuallyhidden focusable" href="#page">
           Skip Navigation
          </a>
          <div class="right_header_container">
           <a class="menu_button" href="javascript:void(0);" id="menu_button">
            <span class="menu_icon">
             menu
            </span>
           </a>
           <a class="modal_close" id="modal_close">
            <span class="modal_close_icon">
            </span>
           </a>
          </div>
          <div class="nav_area">
           <div id="site_nav_container">
            <nav class="site_nav">
             <ul class="nav">
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#red_planet" target="_self">
                 The Red Planet
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/#red_planet/0" target="_self">
                   Dashboard
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/1" target="_self">
                   Science Goals
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/2" target="_self">
                   The Planet
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/3" target="_self">
                   Atmosphere
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/4" target="_self">
                   Astrobiology
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/5" target="_self">
                   Past, Present, Future, Timeline
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#mars_exploration_program" target="_self">
                 The Program
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/#mars_exploration_program/0" target="_self">
                   Mission Statement
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/1" target="_self">
                   About the Program
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/2" target="_self">
                   Organization
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/3" target="_self">
                   Why Mars?
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/4" target="_self">
                   Research Programs
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/5" target="_self">
                   Planetary Resources
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/6" target="_self">
                   Technologies
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#news_and_events" target="_self">
                 News &amp; Events
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li class="current">
                  <a href="/news" target="_self">
                   News
                  </a>
                 </li>
                 <li>
                  <a href="/events" target="_self">
                   Events
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#multimedia" target="_self">
                 Multimedia
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/multimedia/images/" target="_self">
                   Images
                  </a>
                 </li>
                 <li>
                  <a href="/multimedia/videos/" target="_self">
                   Videos
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#missions" target="_self">
                 Missions
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/mars-exploration/missions/?category=167" target="_self">
                   Past
                  </a>
                 </li>
                 <li>
                  <a href="/mars-exploration/missions/?category=170" target="_self">
                   Present
                  </a>
                 </li>
                 <li>
                  <a href="/mars-exploration/missions/?category=171" target="_self">
                   Future
                  </a>
                 </li>
                 <li>
                  <a href="/mars-exploration/partners" target="_self">
                   International Partners
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="nav_title">
                <a class="main_nav_item" href="/#more" target="_self">
                 More
                </a>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="nav_title">
                <a class="main_nav_item" href="/legacy" target="_self">
                 Legacy Site
                </a>
               </div>
               <div class="gradient_line">
               </div>
              </li>
             </ul>
             <form action="https://mars.nasa.gov/search/" class="overlay_search nav_search">
              <label class="search_label">
               Search
              </label>
              <input class="search_field" name="q" type="text" value=""/>
              <div class="search_submit">
              </div>
             </form>
            </nav>
           </div>
          </div>
         </header>
        </div>
        <div id="sticky_nav_spacer">
        </div>
        <div id="page">
         <!-- title to go in the page_header -->
         <div class="header_mask">
         </div>
         <div class="react_grid_list" data-react-class="GridListPage" data-react-props='{"left_column":false,"class_name":"","default_view":"list_view","model":"news_items","view_toggle":false,"search":"true","list_item":"News","title":"News","categories":["19,165,184,204"],"order":"publish_date desc,created_at desc","no_items_text":"There are no items matching these criteria.","per_page":null,"filters":"[ [ \"date\", [ [ \"2018\", \"2018\" ], [ \"2017\", \"2017\" ], [ \"2016\", \"2016\" ], [ \"2015\", \"2015\" ], [ \"2014\", \"2014\" ], [ \"2013\", \"2013\" ], [ \"2012\", \"2012\" ], [ \"2011\", \"2011\" ], [ \"2010\", \"2010\" ], [ \"2009\", \"2009\" ], [ \"2008\", \"2008\" ], [ \"2007\", \"2007\" ], [ \"2006\", \"2006\" ], [ \"2005\", \"2005\" ], [ \"2004\", \"2004\" ], [ \"2003\", \"2003\" ], [ \"2002\", \"2002\" ], [ \"2001\", \"2001\" ], [ \"2000\", \"2000\" ] ], [ \"Latest\", \"\" ], false ], [ \"categories\", [ [ \"Feature Stories\", 165 ], [ \"Press Releases\", 19 ], [ \"Spotlights\", 184 ], [ \"Status Reports\", 204 ] ], [ \"All Categories\", \"\" ], false ] ]","conditions":null,"scope_in_title":true,"options":{"blank_scope":"Latest"},"results_in_title":false}'>
         </div>
         <section class="module suggested_features">
          <div class="grid_layout">
           <header>
            <h2 class="module_title">
             You Might Also Like
            </h2>
           </header>
           <section>
            <script>
             $(document).ready(function(){
        $(".features").slick({
          dots: false,
          infinite: true,
          speed: 300,
          slide: '.features .slide',
          slidesToShow: 3,
          slidesToScroll: 3,
          lazyLoad: 'ondemand',
          centerMode: false,
          arrows: true,
          appendArrows: '.features .slick-nav',
          appendDots: ".features .slick-nav",
          responsive: [{"breakpoint":953,"settings":{"slidesToShow":2,"slidesToScroll":2,"centerMode":false}},{"breakpoint":480,"settings":{"slidesToShow":1,"slidesToScroll":1,"centerMode":true,"arrows":false,"centerPadding":"25px"}}]
        });
      });
            </script>
            <div class="features">
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8348/opportunity-hunkers-down-during-dust-storm/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  As of Tuesday morning, June 19, the Martian dust storm had grown in size and was officially a "planet-encircling" (or "global") dust event.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="Opportunity Hunkers Down During Dust Storm" class="img-lazy" data-lazy="/system/news_items/list_view_images/8348_PIA22521-320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8348/opportunity-hunkers-down-during-dust-storm/">
                Opportunity Hunkers Down During Dust Storm
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8347/nasa-finds-ancient-organic-material-mysterious-methane-on-mars/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA’s Curiosity rover has found evidence on Mars with implications for NASA’s search for life.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA Finds Ancient Organic Material, Mysterious Methane on Mars" class="img-lazy" data-lazy="/system/news_items/list_view_images/8347_curiosity_methane-320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8347/nasa-finds-ancient-organic-material-mysterious-methane-on-mars/">
                NASA Finds Ancient Organic Material, Mysterious Methane on Mars
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8326/nasa-invests-in-visionary-technology/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA is investing in technology concepts, including several from JPL, that may one day be used for future space exploration missions.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA Invests in Visionary Technology " class="img-lazy" data-lazy="/system/news_items/list_view_images/8326_niac320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8326/nasa-invests-in-visionary-technology/">
                NASA Invests in Visionary Technology
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8325/nasa-is-ready-to-study-the-heart-of-mars/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA is about to go on a journey to study the center of Mars.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA is Ready to Study the Heart of Mars" class="img-lazy" data-lazy="/system/news_items/list_view_images/8325_insight20180329b_320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8325/nasa-is-ready-to-study-the-heart-of-mars/">
                NASA is Ready to Study the Heart of Mars
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8322/nasa-briefing-on-first-mission-to-study-mars-interior/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA’s next mission to Mars will be the topic of a media briefing Thursday, March 29, at JPL. The briefing will air live on NASA Television and the agency’s website.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA Briefing on First Mission to Study Mars Interior" class="img-lazy" data-lazy="/system/news_items/list_view_images/8322_PIA22228_320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8322/nasa-briefing-on-first-mission-to-study-mars-interior/">
                NASA Briefing on First Mission to Study Mars Interior
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8321/new-ar-mobile-app-features-3-d-nasa-spacecraft/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA spacecraft travel to far-off destinations in space, but a new mobile app produced by NASA's Jet Propulsion Laboratory, Pasadena, California, brings spacecraft to users.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="New 'AR' Mobile App Features 3-D NASA Spacecraft" class="img-lazy" data-lazy="/system/news_items/list_view_images/8321_list_image.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8321/new-ar-mobile-app-features-3-d-nasa-spacecraft/">
                New 'AR' Mobile App Features 3-D NASA Spacecraft
               </a>
              </div>
             </div>
             <div class="grid_layout">
              <div class="slick-nav_container">
               <div class="slick-nav">
               </div>
              </div>
             </div>
            </div>
           </section>
          </div>
         </section>
        </div>
        <footer id="site_footer">
         <div class="grid_layout">
          <section class="upper_footer">
           <div class="share">
            <h2>
             Follow the Journey
            </h2>
            <div class="social_icons">
             <!-- AddThis Button BEGIN -->
             <div class="addthis_toolbox addthis_default_style addthis_32x32_style">
              <a addthis:userid="NASABeAMartian" class="addthis_button_twitter_follow icon">
               <img alt="twitter" src="/assets/twitter_icon@2x.png"/>
              </a>
              <a addthis:userid="NASABEAM" class="addthis_button_facebook_follow icon">
               <img alt="facebook" src="/assets/facebook_icon@2x.png"/>
              </a>
              <a addthis:userid="nasa" class="addthis_button_instagram_follow icon">
               <img alt="instagram" src="/assets/instagram_icon@2x.png"/>
              </a>
              <a addthis:url="https://mars.nasa.gov/rss/api/?feed=news&amp;category=all&amp;feedtype=rss" class="addthis_button_rss_follow icon">
               <img alt="rss" src="/assets/rss_icon@2x.png"/>
              </a>
             </div>
             <script>
              addthis_loader.init("//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-5a690e4c1320e328", {follow: true})
             </script>
             <!-- AddThis Button END -->
            </div>
           </div>
           <div class="gradient_line">
           </div>
          </section>
          <section class="sitemap">
           <div class="sitemap_directory" id="sitemap_directory">
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#red_planet">
                The Red Planet
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/#red_planet/0" target="_self">
                    Dashboard
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/1" target="_self">
                    Science Goals
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/2" target="_self">
                    The Planet
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/3" target="_self">
                    Atmosphere
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/4" target="_self">
                    Astrobiology
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/5" target="_self">
                    Past, Present, Future, Timeline
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#mars_exploration_program">
                The Program
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/#mars_exploration_program/0" target="_self">
                    Mission Statement
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/1" target="_self">
                    About the Program
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/2" target="_self">
                    Organization
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/3" target="_self">
                    Why Mars?
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/4" target="_self">
                    Research Programs
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/5" target="_self">
                    Planetary Resources
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/6" target="_self">
                    Technologies
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#news_and_events">
                News &amp; Events
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li class="current">
                   <a href="/news" target="_self">
                    News
                   </a>
                  </li>
                  <li>
                   <a href="/events" target="_self">
                    Events
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#multimedia">
                Multimedia
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/multimedia/images/" target="_self">
                    Images
                   </a>
                  </li>
                  <li>
                   <a href="/multimedia/videos/" target="_self">
                    Videos
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#missions">
                Missions
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/mars-exploration/missions/?category=167" target="_self">
                    Past
                   </a>
                  </li>
                  <li>
                   <a href="/mars-exploration/missions/?category=170" target="_self">
                    Present
                   </a>
                  </li>
                  <li>
                   <a href="/mars-exploration/missions/?category=171" target="_self">
                    Future
                   </a>
                  </li>
                  <li>
                   <a href="/mars-exploration/partners" target="_self">
                    International Partners
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#more">
                More
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/legacy">
                Legacy Site
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a class="" href="/legacy" target="_self">
                    Legacy Site
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
           </div>
           <div class="gradient_line">
           </div>
          </section>
          <section class="lower_footer">
           <div class="nav_container">
            <nav>
             <ul>
              <li>
               <a href="http://science.nasa.gov/" target="_blank">
                NASA Science Mission Directorate
               </a>
              </li>
              <li>
               <a href="https://www.jpl.nasa.gov/copyrights.php" target="_blank">
                Privacy
               </a>
              </li>
              <li>
               <a href="http://www.jpl.nasa.gov/imagepolicy/" target="_blank">
                Image Policy
               </a>
              </li>
              <li>
               <a href="https://mars.nasa.gov/feedback/" target="_self">
                Feedback
               </a>
              </li>
              <li>
               <a href="http://mars.nasa.gov/legacy" target="_blank">
                Legacy Mars Site
               </a>
              </li>
             </ul>
            </nav>
           </div>
           <div class="credits">
            <div class="footer_brands_top">
             <p>
              Managed by the Mars Exploration Program and the Jet Propulsion Laboratory for NASA’s Science Mission Directorate
             </p>
            </div>
            <!-- .footer_brands -->
            <!-- %a.jpl{href: "", target: "_blank"}Institution -->
            <!-- -->
            <!-- %a.caltech{href: "", target: "_blank"}Institution -->
            <!-- .staff -->
            <!-- %p -->
            <!-- - get_staff_for_category(get_field_from_admin_config(:web_staff_category_id)) -->
            <!-- - @staff.each_with_index do |staff, idx| -->
            <!-- - unless staff.is_in_footer == 0 -->
            <!-- = staff.title + ": " -->
            <!-- - if staff.contact_link =~ /@/ -->
            <!-- = mail_to staff.contact_link, staff.name, :subject => "[#{@site_title}]" -->
            <!-- - elsif staff.contact_link.present? -->
            <!-- = link_to staff.name, staff.contact_link -->
            <!-- - else -->
            <!-- = staff.name -->
            <!-- - unless (idx + 1 == @staff.size) -->
            <!-- %br -->
           </div>
          </section>
         </div>
        </footer>
       </div>
      </div>
      <script id="_fed_an_ua_tag" src="https://dap.digitalgov.gov/Universal-Federated-Analytics-Min.js?agency=NASA&amp;subagency=JPL-Mars-MEPJPL&amp;pua=UA-9453474-9,UA-118212757-11&amp;dclink=true&amp;sp=searchbox&amp;exts=tif,tiff,wav" type="text/javascript">
      </script>
     </body>
    </html>
    
    


```python
# Extract the title of the HTML document
news_title=soup.find(class_="content_title").text
news_title=news_title.strip('\n')
print(news_title)
```

    Opportunity Hunkers Down During Dust Storm
    


```python

news_p=soup.find(class_="rollover_description_inner").text
news_p=news_p.strip('\n')
print(news_p)
```

    As of Tuesday morning, June 19, the Martian dust storm had grown in size and was officially a "planet-encircling" (or "global") dust event. 
    


```python
executable_path = {'executable_path': 'chromedriver.exe'}
browser = Browser('chrome', **executable_path, headless=False)
```


```python
#Scrape JPL featured Space Image
# URL of page to be scraped
url = 'https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars'
browser.visit(url)
```


```python
# Get the URL for the Full Image of the Featured Space Image
html = browser.html
browser.click_link_by_partial_text('FULL IMAGE')
featured_image_url = browser.find_by_css('.fancybox-image').first['src']
print(featured_image_url)
```

    https://www.jpl.nasa.gov/spaceimages/images/mediumsize/PIA19108_ip.jpg
    


```python
browser.quit()
```


```python
#Scrape Mars Weather Twitter Account
# URL of page to be scraped
url = 'https://twitter.com/marswxreport?lang=en'
```


```python
# Retrieve page with the requests module
response = requests.get(url)
```


```python
# Create BeautifulSoup object; parse with 'html.parser'
soup = BeautifulSoup(response.text, 'html.parser')
```


```python
# Examine the results, then determine element that contains sought info
print(soup.prettify())
```

    <!DOCTYPE html>
    <html data-scribe-reduced-action-queue="true" lang="en">
     <head>
      <meta charset="utf-8"/>
      <script nonce="PeUDRaiStuwOZAAqPmP9Nw==">
       !function(){window.initErrorstack||(window.initErrorstack=[]),window.onerror=function(r,i,n,o,t){r.indexOf("Script error.")>-1||window.initErrorstack.push({errorMsg:r,url:i,lineNumber:n,column:o,errorObj:t})}}();
      </script>
      <script id="bouncer_terminate_iframe" nonce="PeUDRaiStuwOZAAqPmP9Nw==">
       if (window.top != window) {
      window.top.postMessage({'bouncer': true, 'event': 'complete'}, '*');
    }
      </script>
      <script id="swift_action_queue" nonce="PeUDRaiStuwOZAAqPmP9Nw==">
       !function(){function e(e){if(e||(e=window.event),!e)return!1;if(e.timestamp=(new Date).getTime(),!e.target&&e.srcElement&&(e.target=e.srcElement),document.documentElement.getAttribute("data-scribe-reduced-action-queue"))for(var t=e.target;t&&t!=document.body;){if("A"==t.tagName)return;t=t.parentNode}return i("all",o(e)),a(e)?(document.addEventListener||(e=o(e)),e.preventDefault=e.stopPropagation=e.stopImmediatePropagation=function(){},y?(v.push(e),i("captured",e)):i("ignored",e),!1):(i("direct",e),!0)}function t(e){n();for(var t,r=0;t=v[r];r++){var a=e(t.target),i=a.closest("a")[0];if("click"==t.type&&i){var o=e.data(i,"events"),u=o&&o.click,c=!i.hostname.match(g)||!i.href.match(/#$/);if(!u&&c){window.location=i.href;continue}}a.trigger(e.event.fix(t))}window.swiftActionQueue.wasFlushed=!0}function r(){for(var e in b)if("all"!=e)for(var t=b[e],r=0;r<t.length;r++)console.log("actionQueue",c(t[r]))}function n(){clearTimeout(w);for(var e,t=0;e=h[t];t++)document["on"+e]=null}function a(e){if(!e.target)return!1;var t=e.target,r=(t.tagName||"").toLowerCase();if(e.metaKey)return!1;if(e.shiftKey&&"a"==r)return!1;if(t.hostname&&!t.hostname.match(g))return!1;if(e.type.match(p)&&s(t))return!1;if("label"==r){var n=t.getAttribute("for");if(n){var a=document.getElementById(n);if(a&&f(a))return!1}else for(var i,o=0;i=t.childNodes[o];o++)if(f(i))return!1}return!0}function i(e,t){t.bucket=e,b[e].push(t)}function o(e){var t={};for(var r in e)t[r]=e[r];return t}function u(e){for(;e&&e!=document.body;){if("A"==e.tagName)return e;e=e.parentNode}}function c(e){var t=[];e.bucket&&t.push("["+e.bucket+"]"),t.push(e.type);var r,n,a=e.target,i=u(a),o="",c=e.timestamp&&e.timestamp-d;return"click"===e.type&&i?(r=i.className.trim().replace(/\s+/g,"."),n=i.id.trim(),o=/[^#]$/.test(i.href)?" ("+i.href+")":"",a='"'+i.innerText.replace(/\n+/g," ").trim()+'"'):(r=a.className.trim().replace(/\s+/g,"."),n=a.id.trim(),a=a.tagName.toLowerCase(),e.keyCode&&(a=String.fromCharCode(e.keyCode)+" : "+a)),t.push(a+o+(n&&"#"+n)+(!n&&r?"."+r:"")),c&&t.push(c),t.join(" ")}function f(e){var t=(e.tagName||"").toLowerCase();return"input"==t&&"checkbox"==e.getAttribute("type")}function s(e){var t=(e.tagName||"").toLowerCase();return"textarea"==t||"input"==t&&"text"==e.getAttribute("type")||"true"==e.getAttribute("contenteditable")}for(var m,d=(new Date).getTime(),l=1e4,g=/^([^\.]+\.)*twitter\.com$/,p=/^key/,h=["click","keydown","keypress","keyup"],v=[],w=null,y=!0,b={captured:[],ignored:[],direct:[],all:[]},k=0;m=h[k];k++)document["on"+m]=e;w=setTimeout(function(){y=!1},l),window.swiftActionQueue={buckets:b,flush:t,logActions:r,wasFlushed:!1}}();
      </script>
      <script id="composition_state" nonce="PeUDRaiStuwOZAAqPmP9Nw==">
       !function(){function t(t){t.target.setAttribute("data-in-composition","true")}function n(t){t.target.removeAttribute("data-in-composition")}document.addEventListener&&(document.addEventListener("compositionstart",t,!1),document.addEventListener("compositionend",n,!1))}();
      </script>
      <link class="coreCSSBundles" href="https://abs.twimg.com/a/1531883619/css/t1/twitter_core.bundle.css" rel="stylesheet"/>
      <link class="moreCSSBundles" href="https://abs.twimg.com/a/1531883619/css/t1/twitter_more_1.bundle.css" rel="stylesheet"/>
      <link class="moreCSSBundles" href="https://abs.twimg.com/a/1531883619/css/t1/twitter_more_2.bundle.css" rel="stylesheet"/>
      <link href="https://pbs.twimg.com" rel="dns-prefetch"/>
      <link href="https://t.co" rel="dns-prefetch"/>
      <link as="script" href="https://abs.twimg.com/k/en/init.en.3522ca3d1d205f226eb9.js" rel="preload"/>
      <link as="script" href="https://abs.twimg.com/k/en/0.commons.en.dc15f3fe298863985d75.js" rel="preload"/>
      <link as="script" href="https://abs.twimg.com/k/en/3.pages_profile.en.0b0807e07fe459ee1c36.js" rel="preload"/>
      <title>
       Mars Weather (@MarsWxReport) | Twitter
      </title>
      <meta content="NOODP" name="robots"/>
      <meta content="The latest Tweets from Mars Weather (@MarsWxReport). Updates as avail from the REMS weather instrument aboard @MarsCuriosity.  Data credit: Centro deAstrobiologia, FMI, JPL/NASA, Not an official acct. Gale Crater, Mars" name="description"/>
      <meta content="//abs.twimg.com/favicons/win8-tile-144.png" name="msapplication-TileImage">
       <meta content="#00aced" name="msapplication-TileColor">
        <link color="#1da1f2" href="https://abs.twimg.com/a/1531883619/icons/favicon.svg" rel="mask-icon" sizes="any"/>
        <link href="//abs.twimg.com/favicons/favicon.ico" rel="shortcut icon" type="image/x-icon"/>
        <link href="https://abs.twimg.com/icons/apple-touch-icon-192x192.png" rel="apple-touch-icon" sizes="192x192"/>
        <link href="/manifest.json" rel="manifest"/>
        <meta content="profile" id="swift-page-name" name="swift-page-name"/>
        <meta content="profile" id="swift-section-name" name="swift-page-section"/>
        <link href="https://twitter.com/marswxreport" rel="canonical"/>
        <link href="https://twitter.com/marswxreport" hreflang="x-default" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=fr" hreflang="fr" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=en" hreflang="en" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ar" hreflang="ar" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ja" hreflang="ja" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=es" hreflang="es" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=de" hreflang="de" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=it" hreflang="it" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=id" hreflang="id" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=pt" hreflang="pt" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ko" hreflang="ko" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=tr" hreflang="tr" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ru" hreflang="ru" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=nl" hreflang="nl" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=fil" hreflang="fil" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ms" hreflang="ms" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=zh-tw" hreflang="zh-tw" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=zh-cn" hreflang="zh-cn" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=hi" hreflang="hi" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=no" hreflang="no" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=sv" hreflang="sv" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=fi" hreflang="fi" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=da" hreflang="da" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=pl" hreflang="pl" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=hu" hreflang="hu" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=fa" hreflang="fa" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=he" hreflang="he" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ur" hreflang="ur" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=th" hreflang="th" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=uk" hreflang="uk" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ca" hreflang="ca" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ga" hreflang="ga" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=el" hreflang="el" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=eu" hreflang="eu" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=cs" hreflang="cs" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=gl" hreflang="gl" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ro" hreflang="ro" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=hr" hreflang="hr" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=en-gb" hreflang="en-gb" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=vi" hreflang="vi" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=bn" hreflang="bn" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=bg" hreflang="bg" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=sr" hreflang="sr" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=sk" hreflang="sk" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=gu" hreflang="gu" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=mr" hreflang="mr" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=ta" hreflang="ta" rel="alternate"/>
        <link href="https://twitter.com/marswxreport?lang=kn" hreflang="kn" rel="alternate"/>
        <link href="https://publish.twitter.com/oembed?url=https://twitter.com/MarsWxReport" rel="alternate" title="Mars Weather (@MarsWxReport) | Twitter" type="application/json+oembed"/>
        <link href="https://mobile.twitter.com/marswxreport?locale=en" media="handheld, only screen and (max-width: 640px)" rel="alternate"/>
        <link href="android-app://com.twitter.android/twitter/user?screen_name=MarsWxReport&amp;ref_src=twsrc%5Egoogle%7Ctwcamp%5Eandroidseo%7Ctwgr%5Eprofile" rel="alternate"/>
        <link href="/opensearch.xml" rel="search" title="Twitter" type="application/opensearchdescription+xml"/>
        <link id="async-css-placeholder"/>
        <meta content="twitter://user?screen_name=MarsWxReport" property="al:ios:url"/>
        <meta content="333903271" property="al:ios:app_store_id"/>
        <meta content="Twitter" property="al:ios:app_name"/>
        <meta content="twitter://user?screen_name=MarsWxReport" property="al:android:url"/>
        <meta content="com.twitter.android" property="al:android:package"/>
        <meta content="Twitter" property="al:android:app_name"/>
       </meta>
      </meta>
     </head>
     <body class="three-col logged-out user-style-MarsWxReport enhanced-mini-profile ProfilePage ProfilePage--withWarning" data-fouc-class-names="swift-loading no-nav-banners" dir="ltr">
      <script id="swift_loading_indicator" nonce="PeUDRaiStuwOZAAqPmP9Nw==">
       document.body.className=document.body.className+" "+document.body.getAttribute("data-fouc-class-names");
      </script>
      <noscript>
       <form action="https://mobile.twitter.com/i/nojs_router?path=%2Fmarswxreport&amp;lang=en" class="NoScriptForm" method="POST">
        <input name="authenticity_token" type="hidden" value="a1ca0d3455f25d81a0cd641472264bf8915226e3"/>
        <div class="NoScriptForm-content">
         <span class="NoScriptForm-logo Icon Icon--logo Icon--extraLarge">
         </span>
         <p>
          We've detected that JavaScript is disabled in your browser. Would you like to proceed to legacy Twitter?
         </p>
         <p class="NoScriptForm-buttonContainer">
          <button class="EdgeButton EdgeButton--primary" type="submit">
           Yes
          </button>
         </p>
        </div>
       </form>
      </noscript>
      <a class="u-hiddenVisually focusable" href="#timeline">
       Skip to content
      </a>
      <div class="route-profile" data-at-shortcutkeys='{"Enter":"Open Tweet details","o":"Expand photo","/":"Search","?":"This menu","j":"Next Tweet","k":"Previous Tweet","Space":"Page down",".":"Load new Tweets","gu":"Go to user\u2026"}' id="doc">
       <div class="topbar js-topbar">
        <div class="global-nav global-nav--newLoggedOut" data-section-term="top_nav">
         <div class="global-nav-inner">
          <div class="container">
           <ul class="nav js-global-actions" id="global-actions" role="navigation">
            <li class="home" data-global-action="home" id="global-nav-home">
             <a class="js-nav js-tooltip js-dynamic-tooltip" data-component-context="home_nav" data-nav="home" data-placement="bottom" href="/">
              <span class="Icon Icon--bird Icon--large">
              </span>
              <span aria-hidden="true" class="text">
               Home
              </span>
              <span class="u-hiddenVisually a11y-inactive-page-text">
               Home
              </span>
              <span class="u-hiddenVisually a11y-active-page-text">
               Home, current page.
              </span>
             </a>
            </li>
            <li class="moments" data-global-action="moments" id="global-nav-moments">
             <a class="js-nav js-tooltip js-dynamic-tooltip" data-component-context="moments_nav" data-nav="moments" data-placement="bottom" href="/i/moments">
              <span class="Icon Icon--lightning Icon--large">
              </span>
              <span class="Icon Icon--lightningFilled Icon--large">
              </span>
              <span aria-hidden="true" class="text">
               Moments
              </span>
              <span class="u-hiddenVisually a11y-inactive-page-text">
               Moments
              </span>
              <span class="u-hiddenVisually a11y-active-page-text">
               Moments, current page.
              </span>
             </a>
            </li>
           </ul>
           <div class="pull-right nav-extras">
            <div role="search">
             <form action="/search" class="t1-form form-search js-search-form" id="global-nav-search">
              <label class="visuallyhidden" for="search-query">
               Search query
              </label>
              <input autocomplete="off" class="search-input" id="search-query" name="q" placeholder="Search Twitter" spellcheck="false" type="text"/>
              <span class="search-icon js-search-action">
               <button class="Icon Icon--medium Icon--search nav-search" type="submit">
                <span class="visuallyhidden">
                 Search Twitter
                </span>
               </button>
              </span>
              <div class="dropdown-menu typeahead" role="listbox">
               <div aria-hidden="true" class="dropdown-caret">
                <div class="caret-outer">
                </div>
                <div class="caret-inner">
                </div>
               </div>
               <div class="dropdown-inner js-typeahead-results" role="presentation">
                <div class="typeahead-saved-searches" role="presentation">
                 <h3 class="typeahead-category-title saved-searches-title" id="saved-searches-heading">
                  Saved searches
                 </h3>
                 <ul class="typeahead-items saved-searches-list" role="presentation">
                  <li class="typeahead-item typeahead-saved-search-item" role="presentation">
                   <span aria-hidden="true" class="Icon Icon--close">
                    <span class="visuallyhidden">
                     Remove
                    </span>
                   </span>
                   <a aria-describedby="saved-searches-heading" class="js-nav" data-ds="saved_search" data-query-source="" data-search-query="" href="" role="option" tabindex="-1">
                   </a>
                  </li>
                 </ul>
                </div>
                <ul class="typeahead-items typeahead-topics" role="presentation">
                 <li class="typeahead-item typeahead-topic-item" role="presentation">
                  <a class="js-nav" data-ds="topics" data-query-source="typeahead_click" data-search-query="" href="" role="option" tabindex="-1">
                  </a>
                 </li>
                </ul>
                <ul class="typeahead-items typeahead-accounts social-context js-typeahead-accounts" role="presentation">
                 <li class="typeahead-item typeahead-account-item js-selectable" data-remote="true" data-score="" data-user-id="" data-user-screenname="" role="presentation">
                  <a class="js-nav" data-ds="account" data-query-source="typeahead_click" data-search-query="" role="option">
                   <div class="js-selectable typeahead-in-conversation hidden">
                    <span class="Icon Icon--follower Icon--small">
                    </span>
                    <span class="typeahead-in-conversation-text">
                     In this conversation
                    </span>
                   </div>
                   <img alt="" class="avatar size32"/>
                   <span class="typeahead-user-item-info account-group">
                    <span class="fullname">
                    </span>
                    <span class="UserBadges">
                     <span class="Icon Icon--verified js-verified hidden">
                      <span class="u-hiddenVisually">
                       Verified account
                      </span>
                     </span>
                     <span class="Icon Icon--protected js-protected hidden">
                      <span class="u-hiddenVisually">
                       Protected Tweets
                      </span>
                     </span>
                    </span>
                    <span class="UserNameBreak">
                    </span>
                    <span class="username u-dir" dir="ltr">
                     @
                     <b>
                     </b>
                    </span>
                   </span>
                   <span class="typeahead-social-context">
                   </span>
                  </a>
                 </li>
                 <li class="js-selectable typeahead-accounts-shortcut js-shortcut" role="presentation">
                  <a class="js-nav" data-ds="account_search" data-query-source="typeahead_click" data-search-query="" data-shortcut="true" href="" role="option">
                  </a>
                 </li>
                </ul>
                <ul class="typeahead-items typeahead-trend-locations-list" role="presentation">
                 <li class="typeahead-item typeahead-trend-locations-item" role="presentation">
                  <a class="js-nav" data-ds="trend_location" data-search-query="" href="" role="option" tabindex="-1">
                  </a>
                 </li>
                </ul>
                <div class="typeahead-user-select" role="presentation">
                 <div class="typeahead-empty-suggestions" role="presentation">
                  Suggested users
                 </div>
                 <ul class="typeahead-items typeahead-selected js-typeahead-selected" role="presentation">
                  <li class="typeahead-item typeahead-selected-item js-selectable" data-remote="true" data-score="" data-user-id="" data-user-screenname="" role="presentation">
                   <a class="js-nav" data-ds="account" data-query-source="typeahead_click" data-search-query="" role="option">
                    <img alt="" class="avatar size32"/>
                    <span class="typeahead-user-item-info account-group">
                     <span class="select-status deselect-user js-deselect-user Icon Icon--check">
                     </span>
                     <span class="select-status select-disabled Icon Icon--unfollow">
                     </span>
                     <span class="fullname">
                     </span>
                     <span class="UserBadges">
                      <span class="Icon Icon--verified js-verified hidden">
                       <span class="u-hiddenVisually">
                        Verified account
                       </span>
                      </span>
                      <span class="Icon Icon--protected js-protected hidden">
                       <span class="u-hiddenVisually">
                        Protected Tweets
                       </span>
                      </span>
                     </span>
                     <span class="UserNameBreak">
                     </span>
                     <span class="username u-dir" dir="ltr">
                      @
                      <b>
                      </b>
                     </span>
                    </span>
                   </a>
                  </li>
                  <li class="typeahead-selected-end" role="presentation">
                  </li>
                 </ul>
                 <ul class="typeahead-items typeahead-accounts js-typeahead-accounts" role="presentation">
                  <li class="typeahead-item typeahead-account-item js-selectable" data-remote="true" data-score="" data-user-id="" data-user-screenname="" role="presentation">
                   <a class="js-nav" data-ds="account" data-query-source="typeahead_click" data-search-query="" role="option">
                    <img alt="" class="avatar size32"/>
                    <span class="typeahead-user-item-info account-group">
                     <span class="select-status deselect-user js-deselect-user Icon Icon--check">
                     </span>
                     <span class="select-status select-disabled Icon Icon--unfollow">
                     </span>
                     <span class="fullname">
                     </span>
                     <span class="UserBadges">
                      <span class="Icon Icon--verified js-verified hidden">
                       <span class="u-hiddenVisually">
                        Verified account
                       </span>
                      </span>
                      <span class="Icon Icon--protected js-protected hidden">
                       <span class="u-hiddenVisually">
                        Protected Tweets
                       </span>
                      </span>
                     </span>
                     <span class="UserNameBreak">
                     </span>
                     <span class="username u-dir" dir="ltr">
                      @
                      <b>
                      </b>
                     </span>
                    </span>
                   </a>
                  </li>
                  <li class="typeahead-accounts-end" role="presentation">
                  </li>
                 </ul>
                </div>
                <div class="typeahead-dm-conversations" role="presentation">
                 <ul class="typeahead-items typeahead-dm-conversation-items" role="presentation">
                  <li class="typeahead-item typeahead-dm-conversation-item" role="presentation">
                   <a role="option" tabindex="-1">
                   </a>
                  </li>
                 </ul>
                </div>
               </div>
              </div>
             </form>
            </div>
            <ul class="nav secondary-nav language-dropdown">
             <li class="dropdown js-language-dropdown">
              <a class="dropdown-toggle js-dropdown-toggle" href="#supported_languages">
               <small>
                Language:
               </small>
               <span class="js-current-language">
                English
               </span>
               <b class="caret">
               </b>
              </a>
              <div class="dropdown-menu dropdown-menu--rightAlign is-forceRight">
               <div class="dropdown-caret right">
                <span class="caret-outer">
                </span>
                <span class="caret-inner">
                </span>
               </div>
               <ul id="supported_languages">
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="id" href="?lang=id" rel="noopener" title="Indonesian">
                  Bahasa Indonesia
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="msa" href="?lang=msa" rel="noopener" title="Malay">
                  Bahasa Melayu
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ca" href="?lang=ca" rel="noopener" title="Catalan">
                  Català
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="cs" href="?lang=cs" rel="noopener" title="Czech">
                  Čeština
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="da" href="?lang=da" rel="noopener" title="Danish">
                  Dansk
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="de" href="?lang=de" rel="noopener" title="German">
                  Deutsch
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="en-gb" href="?lang=en-gb" rel="noopener" title="British English">
                  English UK
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="es" href="?lang=es" rel="noopener" title="Spanish">
                  Español
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="fil" href="?lang=fil" rel="noopener" title="Filipino">
                  Filipino
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="fr" href="?lang=fr" rel="noopener" title="French">
                  Français
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="hr" href="?lang=hr" rel="noopener" title="Croatian">
                  Hrvatski
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="it" href="?lang=it" rel="noopener" title="Italian">
                  Italiano
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="hu" href="?lang=hu" rel="noopener" title="Hungarian">
                  Magyar
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="nl" href="?lang=nl" rel="noopener" title="Dutch">
                  Nederlands
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="no" href="?lang=no" rel="noopener" title="Norwegian">
                  Norsk
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="pl" href="?lang=pl" rel="noopener" title="Polish">
                  Polski
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="pt" href="?lang=pt" rel="noopener" title="Portuguese">
                  Português
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ro" href="?lang=ro" rel="noopener" title="Romanian">
                  Română
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="sk" href="?lang=sk" rel="noopener" title="Slovak">
                  Slovenčina
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="fi" href="?lang=fi" rel="noopener" title="Finnish">
                  Suomi
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="sv" href="?lang=sv" rel="noopener" title="Swedish">
                  Svenska
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="vi" href="?lang=vi" rel="noopener" title="Vietnamese">
                  Tiếng Việt
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="tr" href="?lang=tr" rel="noopener" title="Turkish">
                  Türkçe
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="el" href="?lang=el" rel="noopener" title="Greek">
                  Ελληνικά
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="bg" href="?lang=bg" rel="noopener" title="Bulgarian">
                  Български език
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ru" href="?lang=ru" rel="noopener" title="Russian">
                  Русский
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="sr" href="?lang=sr" rel="noopener" title="Serbian">
                  Српски
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="uk" href="?lang=uk" rel="noopener" title="Ukrainian">
                  Українська мова
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="he" href="?lang=he" rel="noopener" title="Hebrew">
                  עִבְרִית
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ar" href="?lang=ar" rel="noopener" title="Arabic">
                  العربية
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="fa" href="?lang=fa" rel="noopener" title="Persian">
                  فارسی
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="mr" href="?lang=mr" rel="noopener" title="Marathi">
                  मराठी
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="hi" href="?lang=hi" rel="noopener" title="Hindi">
                  हिन्दी
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="bn" href="?lang=bn" rel="noopener" title="Bangla">
                  বাংলা
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="gu" href="?lang=gu" rel="noopener" title="Gujarati">
                  ગુજરાતી
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ta" href="?lang=ta" rel="noopener" title="Tamil">
                  தமிழ்
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="kn" href="?lang=kn" rel="noopener" title="Kannada">
                  ಕನ್ನಡ
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="th" href="?lang=th" rel="noopener" title="Thai">
                  ภาษาไทย
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ko" href="?lang=ko" rel="noopener" title="Korean">
                  한국어
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="ja" href="?lang=ja" rel="noopener" title="Japanese">
                  日本語
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="zh-cn" href="?lang=zh-cn" rel="noopener" title="Simplified Chinese">
                  简体中文
                 </a>
                </li>
                <li>
                 <a class="js-language-link js-tooltip" data-lang-code="zh-tw" href="?lang=zh-tw" rel="noopener" title="Traditional Chinese">
                  繁體中文
                 </a>
                </li>
               </ul>
              </div>
              <div class="js-front-language">
               <form action="/sessions/change_locale" class="t1-form language" method="POST">
                <input name="lang" type="hidden"/>
                <input name="redirect" type="hidden"/>
                <input name="authenticity_token" type="hidden" value="a1ca0d3455f25d81a0cd641472264bf8915226e3"/>
               </form>
              </div>
             </li>
            </ul>
            <ul class="nav secondary-nav session-dropdown" id="session">
             <li class="dropdown js-session">
              <a class="dropdown-toggle js-dropdown-toggle dropdown-signin" data-nav="login" href="/login" id="signin-link" role="button">
               <small>
                Have an account?
               </small>
               <span class="emphasize">
                Log in
               </span>
               <span class="caret">
               </span>
              </a>
              <div class="dropdown-menu dropdown-form dropdown-menu--rightAlign is-forceRight" id="signin-dropdown">
               <div class="dropdown-caret right">
                <span class="caret-outer">
                </span>
                <span class="caret-inner">
                </span>
               </div>
               <div class="signin-dialog-body">
                <div>
                 Have an account?
                </div>
                <form action="https://twitter.com/sessions" class="LoginForm js-front-signin" data-component="login_callout" data-element="form" method="post">
                 <div class="LoginForm-input LoginForm-username">
                  <input autocomplete="username" class="text-input email-input js-signin-email" name="session[username_or_email]" placeholder="Phone, email, or username" type="text">
                  </input>
                 </div>
                 <div class="LoginForm-input LoginForm-password">
                  <input autocomplete="current-password" class="text-input" name="session[password]" placeholder="Password" type="password"/>
                 </div>
                 <div class="LoginForm-rememberForgot">
                  <label>
                   <input checked="checked" name="remember_me" type="checkbox" value="1"/>
                   <span>
                    Remember me
                   </span>
                  </label>
                  <span class="separator">
                   ·
                  </span>
                  <a class="forgot" href="/account/begin_password_reset" rel="noopener">
                   Forgot password?
                  </a>
                 </div>
                 <input class="EdgeButton EdgeButton--primary EdgeButton--medium submit js-submit" type="submit" value="Log in"/>
                 <input name="return_to_ssl" type="hidden" value="true"/>
                 <input name="scribe_log" type="hidden"/>
                 <input name="redirect_after_login" type="hidden" value="/marswxreport?lang=en"/>
                 <input name="authenticity_token" type="hidden" value="a1ca0d3455f25d81a0cd641472264bf8915226e3"/>
                 <input autocomplete="off" name="ui_metrics" type="hidden"/>
                 <script async="" src="/i/js_inst?c_name=ui_metrics">
                 </script>
                </form>
                <hr/>
                <div class="signup SignupForm">
                 <div class="SignupForm-header">
                  New to Twitter?
                 </div>
                 <a class="EdgeButton EdgeButton--secondary EdgeButton--medium u-block js-signup" data-component="signup_callout" data-element="dropdown" href="https://twitter.com/signup" role="button">
                  Sign up
                 </a>
                </div>
               </div>
              </div>
             </li>
            </ul>
           </div>
          </div>
         </div>
        </div>
       </div>
       <div id="page-outer">
        <div class="AppContent" id="page-container">
         <style id="user-style-MarsWxReport">
          a,
      a:hover,
      a:focus,
      a:active {
        color: #0084B4;
      }
    
      .u-textUserColor,
      .u-textUserColorHover:hover,
      .u-textUserColorHover:hover .ProfileTweet-actionCount,
      .u-textUserColorHover:focus {
        color: #0084B4 !important;
      }
    
      .u-borderUserColor,
      .u-borderUserColorHover:hover,
      .u-borderUserColorHover:focus {
        border-color: #0084B4 !important;
      }
    
      .u-bgUserColor,
      .u-bgUserColorHover:hover,
      .u-bgUserColorHover:focus {
        background-color: #0084B4 !important;
      }
    
      .u-dropdownUserColor > li:hover,
      .u-dropdownUserColor > li:focus,
      .u-dropdownUserColor > li > button:hover,
      .u-dropdownUserColor > li > button:focus,
      .u-dropdownUserColor > li > a:focus,
      .u-dropdownUserColor > li > a:hover {
        color: #fff !important;
        background-color: #0084B4 !important;
      }
    
      .u-boxShadowInsetUserColorHover:hover,
      .u-boxShadowInsetUserColorHover:focus {
        box-shadow: inset 0 0 0 5px #0084B4 !important;
      }
    
      .u-dropdownOpenUserColor.dropdown.open .dropdown-toggle {
        color: #0084B4;
      }
    
    
      .u-textUserColorLight {
        color: #99CDE1 !important;
      }
    
      .u-borderUserColorLight,
      .u-borderUserColorLightFocus:focus,
      .u-borderUserColorLightHover:hover,
      .u-borderUserColorLightHover:focus {
        border-color: #99CDE1 !important;
      }
    
      .u-bgUserColorLight {
        background-color: #99CDE1 !important;
      }
    
    
      .u-boxShadowUserColorLighterFocus:focus {
        box-shadow: 0 0 8px rgba(0, 0, 0, 0.05), inset 0 1px 2px rgba(0,132,180,0.25) !important;
      }
    
    
      .u-textUserColorLightest {
        color: #E5F2F7 !important;
      }
    
      .u-borderUserColorLightest {
        border-color: #E5F2F7 !important;
      }
    
      .u-bgUserColorLightest {
        background-color: #E5F2F7 !important;
      }
    
    
      .u-textUserColorLighter {
        color: #BFE0EC !important;
      }
    
      .u-borderUserColorLighter {
        border-color: #BFE0EC !important;
      }
    
      .u-bgUserColorLighter {
        background-color: #BFE0EC !important;
      }
    
    
      .u-bgUserColorDarkHover:hover {
        background-color: #05719A !important;
      }
    
      .u-borderUserColorDark {
        border-color: #05719A !important;
      }
    
    
      .u-bgUserColorDarkerActive:active {
        background-color: #0A5F81 !important;
      }
    
    
    
    
    
    
    
    
    
    
    
    
    
    a,
    .btn-link,
    .btn-link:focus,
    .icon-btn,
    
    
    
    .pretty-link b,
    .pretty-link:hover s,
    .pretty-link:hover b,
    .pretty-link:focus s,
    .pretty-link:focus b,
    
    .metadata a:hover,
    .metadata a:focus,
    
    a.account-group:hover .fullname,
    a.account-group:focus .fullname,
    .account-summary:focus .fullname,
    
    .message .message-text a,
    .message .message-text button,
    .stats a strong,
    .plain-btn:hover,
    .plain-btn:focus,
    .dropdown.open .user-dropdown.plain-btn,
    .open > .plain-btn,
    #global-actions .new:before,
    .module .list-link:hover,
    .module .list-link:focus,
    
    .stats a:hover,
    .stats a:hover strong,
    .stats a:focus,
    .stats a:focus strong,
    
    .find-friends-sources li:hover .source,
    
    
    
    
    
    .stream-item a:hover .fullname,
    .stream-item a:focus .fullname,
    
    .stream-item .view-all-supplements:hover,
    .stream-item .view-all-supplements:focus,
    
    .tweet .time a:hover,
    .tweet .time a:focus,
    .tweet .details.with-icn b,
    .tweet .details.with-icn .Icon,
    
    .stream-item:hover .original-tweet .details b,
    .stream-item .original-tweet.focus .details b,
    .stream-item.open .original-tweet .details b,
    
    .client-and-actions a:hover,
    .client-and-actions a:focus,
    
    .dismiss-btn:hover b,
    
    .tweet .context .pretty-link:hover s,
    .tweet .context .pretty-link:hover b,
    .tweet .context .pretty-link:focus s,
    .tweet .context .pretty-link:focus b,
    
    .list .username a:hover,
    .list .username a:focus,
    .list-membership-container .create-a-list,
    .list-membership-container .create-a-list:hover,
    .new-tweets-bar,
    
    
    
    .card .list-details a:hover,
    .card .list-details a:focus,
    .card .card-body:hover .attribution,
    .card .card-body .attribution:focus {
      color: #0084B4;
    }
    
    
    
    
      
      .FoundMediaSearch--keyboard .FoundMediaSearch-focusable.is-focused {
        border-color: #0084B4;
      }
    
      
      .photo-selector:hover .btn,
      .icon-btn:hover,
      .icon-btn:active,
      .icon-btn.active,
      .icon-btn.enabled {
        border-color: #0084B4;
        border-color: rgba(0,132,180,0.4);
        color: #0084B4;
      }
    
      
      .photo-selector:hover .btn,
      .icon-btn:hover {
        background-image: linear-gradient(rgba(255,255,255,0), rgba(0,132,180,0.1));
      }
    
      .icon-btn.disabled,
      .icon-btn.disabled:hover,
      .icon-btn[disabled],
      .icon-btn[aria-disabled=true] {
        color: #0084B4;
      }
    
      
      
    
      .EdgeButton--primary,
      .EdgeButton--primary:focus {
        background-color: #329CC3;
        border-color: transparent;
      }
    
      .EdgeButton--primary:hover,
      .EdgeButton--primary:active {
        background-color: #0084B4;
        border-color: #0084B4;
      }
    
      .EdgeButton--primary:focus {
        box-shadow:
          0 0 0 2px #FFFFFF,
          0 0 0 4px #99CDE1;
      }
    
      .EdgeButton--primary:active {
        box-shadow:
          0 0 0 2px #FFFFFF,
          0 0 0 4px #329CC3;
      }
    
      
      
    
      .EdgeButton--secondary,
      .EdgeButton--secondary:hover,
      .EdgeButton--secondary:focus,
      .EdgeButton--secondary:active {
        border-color: #0084B4;
        color: #0084B4;
      }
    
      .EdgeButton--secondary:hover,
      .EdgeButton--secondary:active {
        background-color: #E5F2F7;
      }
    
      .EdgeButton--secondary:focus {
        box-shadow:
          0 0 0 2px #FFFFFF,
          0 0 0 4px rgba(0,132,180,0.4);
      }
    
      .EdgeButton--secondary:active {
        box-shadow:
          0 0 0 2px #FFFFFF,
          0 0 0 4px #0084B4;
      }
    
      
      
    
      .EdgeButton--invertedPrimary {
        color: #0084B4 !important;
      }
    
      .EdgeButton--invertedPrimary:focus {
        box-shadow:
          0 0 0 2px #0084B4,
          0 0 0 4px #99CDE1;
      }
    
      .EdgeButton--invertedPrimary:active {
        box-shadow:
          0 0 0 2px #0084B4,
          0 0 0 4px #FFFFFF;
      }
    
      
      
    
      .EdgeButton--invertedSecondary {
        background-color: #0084B4;
      }
    
      .EdgeButton--invertedSecondary:hover {
        background-color: #329CC3;
      }
    
      .EdgeButton--invertedSecondary:focus {
        box-shadow:
          0 0 0 2px #0084B4,
          0 0 0 4px #99CDE1;
      }
    
      .EdgeButton--invertedSecondary:active {
        box-shadow:
          0 0 0 2px #0084B4,
          0 0 0 4px #FFFFFF;
      }
    
      
    
      .btn:focus,
      .btn.focus,
      .Button:focus,
      .EmojiPicker-item.is-focused,
      .EmojiPicker .EmojiCategoryIcon:focus,
      .EmojiPicker-skinTone:focus + .EmojiPicker-skinToneSwatch,
      a:focus > img:first-child:last-child,
      button:focus {
        box-shadow:
          0 0 0 2px #FFFFFF,
          0 0 2px 4px rgba(0,132,180,0.4);
      }
    
      .selected-stream-item:focus {
        box-shadow: 0 0 0 3px rgba(0,132,180,0.4);
      }
    
      
      .js-navigable-stream.stream-table-view .selected-stream-item[tabindex="-1"]:focus {
        outline: 3px solid rgba(0,132,180,0.4) !important;
      }
    
      
      .js-navigable-stream.stream-table-view .selected-stream-item:focus {
        box-shadow: none;
      }
    
      
    
      .global-dm-nav.new.with-count .dm-new .count-inner {
        background: #0084B4;
      }
    
      .global-nav .people .count .count-inner {
        background: #0084B4;
      }
    
      .dropdown-menu li > a:hover,
      .dropdown-menu li > a:focus,
      .dropdown-menu .dropdown-link:hover,
      .dropdown-menu .dropdown-link:focus,
      .dropdown-menu .dropdown-link.is-focused,
      .dropdown-menu li:hover .dropdown-link,
      .dropdown-menu li:focus .dropdown-link,
      .dropdown-menu .selected a,
      .dropdown-menu .dropdown-link.selected {
        background-color: #0084B4 !important;
      }
    
      /* for items in typeahead dropdown menu on logged in pages */
      .dropdown-menu .typeahead-items li > a:focus,
      .dropdown-menu .typeahead-items li > a:hover,
      .dropdown-menu .typeahead-items .selected,
      .dropdown-menu .typeahead-items .selected a {
        background-color: #E5F2F7 !important;
        color: #0084B4 !important;
      }
    
      .typeahead a:hover,
      .typeahead a:hover strong,
      .typeahead a:hover .fullname,
      .typeahead .selected a,
      .typeahead .selected strong,
      .typeahead .selected .fullname,
      .typeahead .selected .Icon--close {
        color: #0084B4 !important;
      }
    
    
    .home-tweet-box,
    .LiveVideo-tweetBox,
    .RetweetDialog-commentBox {
      background-color: #E5F2F7;
    }
    
    .top-timeline-tweetbox .timeline-tweet-box .tweet-form.condensed .tweet-box {
      color: #0084B4;
    }
    
    .RichEditor,
    .TweetBoxAttachments {
      border-color: #BFE0EC;
    }
    
    input:focus,
    textarea:focus,
    div[contenteditable="true"]:focus,
    div[contenteditable="true"].fake-focus,
    div[contenteditable="plaintext-only"]:focus,
    div[contenteditable="plaintext-only"].fake-focus {
      border-color: #99CDE1;
      box-shadow: inset 0 0 0 1px rgba(0,132,180,0.7);
    }
    
    .tweet-box textarea:focus,
    .tweet-box input[type=text],
    .currently-dragging .tweet-form.is-droppable .tweet-drag-help,
    .tweet-box[contenteditable="true"]:focus,
    .RichEditor.is-fakeFocus,
    .RichEditor.is-fakeFocus ~ .TweetBoxAttachments {
      border-color: #99CDE1;
      box-shadow: 0 0 0 1px #99CDE1;
    }
    
    .MomentCapsuleItem.selected-stream-item:focus {
      box-shadow: 0 0 0 3px rgba(0,132,180,0.4);
    }
    
    
    
    
    s,
    .pretty-link:hover s,
    .pretty-link:focus s,
    .stream-item-activity-notification .latest-tweet .tweet-row a:hover s,
    .stream-item-activity-notification .latest-tweet .tweet-row a:focus s {
        color: #0084B4;
    }
    
    
    
    .vellip,
    .vellip:before,
    .vellip:after,
    .conversation-module > li:after,
    .conversation-module > li:before,
    .ThreadedConversation--loneTweet:after,
    .ThreadedConversation-tweet:not(.is-hiddenAncestor) ~ .ThreadedConversation-tweet:before,
    .ThreadedConversation-tweet:after,
    .ThreadedConversation-moreReplies:before,
    .ThreadedConversation-viewOther:before,
    .ThreadedConversation-unavailableTweet:before,
    .ThreadedConversation-unavailableTweet:after,
    .ThreadedConversation--permalinkTweetWithAncestors:before,
    .mini-avatar-with-thread:before,
    .permalink.self-thread-permalink-with-descendant .permalink-tweet-container:after,
    .permalink.self-thread-permalink-with-descendant .inline-reply-tweetbox-container:after {
        border-color: #99CDE1;
    }
    
    
    
    
    .tweet .sm-reply,
    .tweet .sm-rt,
    .tweet .sm-fav,
    .tweet .sm-image,
    .tweet .sm-video,
    .tweet .sm-audio,
    .tweet .sm-geo,
    .tweet .sm-in,
    .tweet .sm-trash,
    .tweet .sm-more,
    .tweet .sm-page,
    .tweet .sm-embed,
    .tweet .sm-summary,
    .tweet .sm-chat,
    
    .timelines-navigation .active .profile-nav-icon,
    .timelines-navigation .profile-nav-icon:hover,
    .timelines-navigation .profile-nav-link:focus .profile-nav-icon,
    
    .sm-top-tweet {
        background-color: #0084B4;
    }
    
    .enhanced-mini-profile .mini-profile .profile-summary {
      background-image: url(https://pbs.twimg.com/profile_banners/786939553/1403835009/mobile);
    }
    
      #global-tweet-dialog .modal-header,
      #Tweetstorm-dialog .modal-header {
        border-bottom: solid 1px rgba(0,132,180,0.25);
      }
    
      #global-tweet-dialog .modal-tweet-form-container,
      #Tweetstorm-dialog .modal-body {
        background-color: #0084B4;
        background: rgba(0,132,180,0.1);
      }
    
      .TweetstormDialog-reply-context .tweet-box-avatar:after,
      .TweetstormDialog-reply-context .tweet-box-avatar:before,
      .TweetstormDialog-tweet-box .tweet-box-avatar:after,
      .TweetstormDialog-tweet-box .tweet-box-avatar:before {
        border-color: #99CDE1;
      }
    
      .global-nav .search-input:focus,
      .global-nav .search-input.focus {
        border: 2px solid #0084B4;
      }
    }
    
      .inline-reply-tweetbox {
        background-color: #E5F2F7;
      }
         </style>
         <div class="ProfileCanopy ProfileCanopy--withNav ProfileCanopy--large js-variableHeightTopBar">
          <div class="ProfileCanopy-inner">
           <div class="ProfileCanopy-header u-bgUserColor">
            <div class="ProfileCanopy-headerBg">
             <img alt="" src="https://pbs.twimg.com/profile_banners/786939553/1403835009/1500x500"/>
            </div>
            <div class="AppContainer">
             <div class="ProfileCanopy-avatar">
              <div class="ProfileAvatar">
               <a class="ProfileAvatar-container u-block js-tooltip profile-picture" data-resolved-url-large="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_400x400.jpg" data-url="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_400x400.jpg" href="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_400x400.jpg" rel="noopener" target="_blank" title="Mars Weather">
                <img alt="Mars Weather" class="ProfileAvatar-image " src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_400x400.jpg"/>
               </a>
              </div>
             </div>
             <div class="ProfileCanopy-headerPromptAnchor">
             </div>
            </div>
           </div>
           <div class="ProfileCanopy-navBar u-boxShadow">
            <div class="AppContainer">
             <div class="Grid Grid--withGutter">
              <div class="Grid-cell u-size1of3 u-lg-size1of4">
               <div class="ProfileCanopy-card" role="presentation">
                <div class="ProfileCardMini">
                 <a class="ProfileCardMini-avatar profile-picture js-tooltip" data-resolved-url-large="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere.jpg" data-url="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere.jpg" href="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere.jpg" rel="noopener" target="_blank" title="Mars Weather">
                  <img alt="Mars Weather" class="ProfileCardMini-avatarImage" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_normal.jpg"/>
                 </a>
                 <div class="ProfileCardMini-details">
                  <div class="ProfileNameTruncated account-group">
                   <div class="u-textTruncate u-inlineBlock">
                    <a class="fullname ProfileNameTruncated-link u-textInheritColor js-nav" data-aria-label-part="" href="/MarsWxReport">
                     Mars Weather
                    </a>
                   </div>
                   <span class="UserBadges">
                   </span>
                  </div>
                  <div class="ProfileCardMini-screenname">
                   <a class="ProfileCardMini-screennameLink u-linkComplex js-nav u-dir" dir="ltr" href="/MarsWxReport">
                    <span class="username u-dir" dir="ltr">
                     @
                     <b class="u-linkComplex-target">
                      MarsWxReport
                     </b>
                    </span>
                   </a>
                  </div>
                 </div>
                </div>
               </div>
              </div>
              <div class="Grid-cell u-size2of3 u-lg-size3of4">
               <div class="ProfileCanopy-nav">
                <div class="ProfileNav" data-user-id="786939553" role="navigation">
                 <ul class="ProfileNav-list">
                  <li class="ProfileNav-item ProfileNav-item--tweets is-active">
                   <a class="ProfileNav-stat ProfileNav-stat--link u-borderUserColor u-textCenter js-tooltip js-nav" data-nav="tweets" tabindex="0" title="1,521 Tweets">
                    <span aria-hidden="true" class="ProfileNav-label">
                     Tweets
                    </span>
                    <span class="u-hiddenVisually">
                     Tweets, current page.
                    </span>
                    <span class="ProfileNav-value" data-count="1521" data-is-compact="false">
                     1,521
                    </span>
                   </a>
                  </li>
                  <li class="ProfileNav-item ProfileNav-item--following">
                   <a class="ProfileNav-stat ProfileNav-stat--link u-borderUserColor u-textCenter js-tooltip js-openSignupDialog js-nonNavigable u-textUserColor" data-nav="following" href="/MarsWxReport/following" title="47 Following">
                    <span aria-hidden="true" class="ProfileNav-label">
                     Following
                    </span>
                    <span class="u-hiddenVisually">
                     Following
                    </span>
                    <span class="ProfileNav-value" data-count="47" data-is-compact="false">
                     47
                    </span>
                   </a>
                  </li>
                  <li class="ProfileNav-item ProfileNav-item--followers">
                   <a class="ProfileNav-stat ProfileNav-stat--link u-borderUserColor u-textCenter js-tooltip js-openSignupDialog js-nonNavigable u-textUserColor" data-nav="followers" href="/MarsWxReport/followers" title="39,016 Followers">
                    <span aria-hidden="true" class="ProfileNav-label">
                     Followers
                    </span>
                    <span class="u-hiddenVisually">
                     Followers
                    </span>
                    <span class="ProfileNav-value" data-count="39016" data-is-compact="true">
                     39K
                    </span>
                   </a>
                  </li>
                  <li class="ProfileNav-item ProfileNav-item--favorites" data-more-item=".ProfileNav-dropdownItem--favorites">
                   <a class="ProfileNav-stat ProfileNav-stat--link u-borderUserColor u-textCenter js-tooltip js-openSignupDialog js-nonNavigable u-textUserColor" data-nav="favorites" href="/MarsWxReport/likes" title="216 Likes">
                    <span aria-hidden="true" class="ProfileNav-label">
                     Likes
                    </span>
                    <span class="u-hiddenVisually">
                     Likes
                    </span>
                    <span class="ProfileNav-value" data-count="216" data-is-compact="false">
                     216
                    </span>
                   </a>
                  </li>
                  <li class="ProfileNav-item ProfileNav-item--lists" data-more-item=".ProfileNav-dropdownItem--lists">
                   <a class="ProfileNav-stat ProfileNav-stat--link u-borderUserColor u-textCenter js-tooltip js-openSignupDialog js-nonNavigable u-textUserColor" data-nav="all_lists" href="/MarsWxReport/lists" title="9 Lists">
                    <span aria-hidden="true" class="ProfileNav-label">
                     Lists
                    </span>
                    <span class="u-hiddenVisually">
                     Lists
                    </span>
                    <span class="ProfileNav-value" data-is-compact="false">
                     9
                    </span>
                   </a>
                  </li>
                  <li class="ProfileNav-item ProfileNav-item--more dropdown is-hidden">
                   <a class="ProfileNav-stat ProfileNav-stat--link ProfileNav-stat--moreLink js-openSignupDialog js-nonNavigable" href="#more" role="button">
                    <span class="ProfileNav-label">
                    </span>
                    <span class="ProfileNav-value">
                     More
                     <span class="ProfileNav-dropdownCaret Icon Icon--medium Icon--caretDown">
                     </span>
                    </span>
                   </a>
                   <div class="dropdown-menu">
                    <div class="dropdown-caret">
                     <span class="caret-outer">
                     </span>
                     <span class="caret-inner">
                     </span>
                    </div>
                    <ul>
                     <li>
                      <a class="ProfileNav-dropdownItem ProfileNav-dropdownItem--favorites is-hidden u-bgUserColorHover u-bgUserColorFocus u-linkClean js-nav" href="/MarsWxReport/likes">
                       Likes
                      </a>
                     </li>
                     <li>
                      <a class="ProfileNav-dropdownItem ProfileNav-dropdownItem--lists is-hidden u-bgUserColorHover u-bgUserColorFocus u-linkClean js-nav" href="/MarsWxReport/lists">
                       Lists
                      </a>
                     </li>
                    </ul>
                   </div>
                  </li>
                  <li class="ProfileNav-item ProfileNav-item--userActions u-floatRight u-textRight with-rightCaret ">
                   <div class="UserActions u-textLeft">
                    <div class="user-actions btn-group not-following " data-name="Mars Weather" data-protected="false" data-screen-name="MarsWxReport" data-user-id="786939553">
                     <span class="UserActions-moreActions u-inlineBlock">
                      <button class="js-tooltip unmute-button btn small plain-btn" data-placement="top" title="Unmute @MarsWxReport" type="button">
                       <span class="Icon Icon--muted Icon--medium">
                        <span class="visuallyhidden">
                         Unmute
                         <span class="username u-dir u-textTruncate" dir="ltr">
                          @
                          <b>
                           MarsWxReport
                          </b>
                         </span>
                        </span>
                       </span>
                      </button>
                      <button class="first-load js-tooltip mute-button btn small plain-btn" data-placement="top" title="Mute @MarsWxReport" type="button">
                       <span class="Icon Icon--unmuted Icon--medium">
                        <span class="visuallyhidden">
                         Mute
                         <span class="username u-dir u-textTruncate" dir="ltr">
                          @
                          <b>
                           MarsWxReport
                          </b>
                         </span>
                        </span>
                       </span>
                      </button>
                     </span>
                     <span class="user-actions-follow-button js-follow-btn follow-button">
                      <button class=" EdgeButton EdgeButton--secondary EdgeButton--medium button-text follow-text" type="button">
                       <span aria-hidden="true">
                        Follow
                       </span>
                       <span class="u-hiddenVisually">
                        Follow
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                      <button class=" EdgeButton EdgeButton--primary EdgeButton--medium button-text following-text" type="button">
                       <span aria-hidden="true">
                        Following
                       </span>
                       <span class="u-hiddenVisually">
                        Following
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                      <button class=" EdgeButton EdgeButton--danger EdgeButton--medium button-text unfollow-text" type="button">
                       <span aria-hidden="true">
                        Unfollow
                       </span>
                       <span class="u-hiddenVisually">
                        Unfollow
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                      <button class=" EdgeButton EdgeButton--invertedDanger EdgeButton--medium button-text blocked-text" type="button">
                       <span aria-hidden="true">
                        Blocked
                       </span>
                       <span class="u-hiddenVisually">
                        Blocked
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                      <button class=" EdgeButton EdgeButton--danger EdgeButton--medium button-text unblock-text" type="button">
                       <span aria-hidden="true">
                        Unblock
                       </span>
                       <span class="u-hiddenVisually">
                        Unblock
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                      <button class=" EdgeButton EdgeButton--secondary EdgeButton--medium button-text pending-text" type="button">
                       <span aria-hidden="true">
                        Pending
                       </span>
                       <span class="u-hiddenVisually">
                        Pending follow request from
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                      <button class=" EdgeButton EdgeButton--secondary EdgeButton--medium button-text cancel-text" type="button">
                       <span aria-hidden="true">
                        Cancel
                       </span>
                       <span class="u-hiddenVisually">
                        Cancel your follow request to
                        <span class="username u-dir u-textTruncate" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </span>
                      </button>
                     </span>
                    </div>
                   </div>
                  </li>
                 </ul>
                </div>
               </div>
              </div>
             </div>
            </div>
           </div>
          </div>
         </div>
         <div class="AppContainer">
          <div aria-labelledby="content-main-heading" class="AppContent-main content-main u-cf" role="main">
           <div class="Grid Grid--withGutter">
            <div class="Grid-cell u-size1of3 u-lg-size1of4">
             <div class="Grid Grid--withGutter">
              <div class="Grid-cell">
               <div class="ProfileSidebar ProfileSidebar--withLeftAlignment">
                <div class="ProfileHeaderCard">
                 <h1 class="ProfileHeaderCard-name">
                  <a class="ProfileHeaderCard-nameLink u-textInheritColor js-nav" href="/MarsWxReport">
                   Mars Weather
                  </a>
                 </h1>
                 <h2 class="ProfileHeaderCard-screenname u-inlineBlock u-dir" dir="ltr">
                  <a class="ProfileHeaderCard-screennameLink u-linkComplex js-nav" href="/MarsWxReport">
                   <span class="username u-dir" dir="ltr">
                    @
                    <b class="u-linkComplex-target">
                     MarsWxReport
                    </b>
                   </span>
                  </a>
                 </h2>
                 <p class="ProfileHeaderCard-bio u-dir" dir="ltr">
                  Updates as avail from the REMS weather instrument aboard
                  <a class="tweet-url twitter-atreply pretty-link" data-mentioned-user-id="0" dir="ltr" href="/MarsCuriosity" rel="nofollow">
                   <s>
                    @
                   </s>
                   <b>
                    MarsCuriosity
                   </b>
                  </a>
                  .  Data credit: Centro deAstrobiologia, FMI, JPL/NASA, Not an official acct.
                 </p>
                 <div class="ProfileHeaderCard-location ">
                  <span aria-hidden="true" class="Icon Icon--geo Icon--medium" role="presentation">
                  </span>
                  <span class="ProfileHeaderCard-locationText u-dir" dir="ltr">
                   Gale Crater, Mars
                  </span>
                 </div>
                 <div class="ProfileHeaderCard-url ">
                  <span aria-hidden="true" class="Icon Icon--url Icon--medium" role="presentation">
                  </span>
                  <span class="ProfileHeaderCard-urlText u-dir">
                   <a class="u-textUserColor" href="http://t.co/OcX0oySes3" rel="me nofollow noopener" target="_blank" title="http://mars.nasa.gov/msl/mission/instruments/environsensors/rems/">
                    mars.nasa.gov/msl/mission/in…
                   </a>
                  </span>
                 </div>
                 <div class="ProfileHeaderCard-joinDate">
                  <span aria-hidden="true" class="Icon Icon--calendar Icon--medium" role="presentation">
                  </span>
                  <span class="ProfileHeaderCard-joinDateText js-tooltip u-dir" dir="ltr" title="5:48 AM - 28 Aug 2012">
                   Joined August 2012
                  </span>
                 </div>
                 <div class="ProfileHeaderCard-birthdate u-hidden">
                  <span aria-hidden="true" class="Icon Icon--balloon Icon--medium" role="presentation">
                  </span>
                  <span class="ProfileHeaderCard-birthdateText u-dir" dir="ltr">
                  </span>
                 </div>
                </div>
                <div class="PhotoRail">
                 <div class="PhotoRail-heading">
                  <span aria-hidden="true" class="Icon Icon--camera Icon--medium" role="presentation">
                  </span>
                  <span class="PhotoRail-headingText">
                   <a class="PhotoRail-headingWithCount js-nav" href="/MarsWxReport/media">
                    189 Photos and videos
                   </a>
                   <a class="PhotoRail-headingWithoutCount js-nav" href="/MarsWxReport/media">
                    Photos and videos
                   </a>
                  </span>
                 </div>
                 <div class="PhotoRail-mediaBox">
                  <span class="js-photoRailInsertPoint">
                  </span>
                 </div>
                </div>
               </div>
              </div>
             </div>
            </div>
            <div class="Grid-cell u-size2of3 u-lg-size3of4">
             <div class="Grid Grid--withGutter">
              <div class="Grid-cell">
               <div class="js-profileClusterFollow">
               </div>
              </div>
              <div class="Grid-cell u-lg-size2of3 " data-test-selector="ProfileTimeline">
               <div class="ProfileHeading">
                <div class="ProfileHeading-spacer">
                </div>
                <div class="ProfileHeading-content">
                 <h2 class="ProfileHeading-title u-hiddenVisually " id="content-main-heading">
                  Tweets
                 </h2>
                 <ul class="ProfileHeading-toggle">
                  <li class="ProfileHeading-toggleItem is-active" data-element-term="tweets_toggle">
                   <span aria-hidden="true">
                    Tweets
                   </span>
                   <span class="u-hiddenVisually">
                    Tweets, current page.
                   </span>
                  </li>
                  <li class="ProfileHeading-toggleItem u-textUserColor" data-element-term="tweets_with_replies_toggle">
                   <a class="ProfileHeading-toggleLink js-openSignupDialog js-nonNavigable" data-nav="tweets_with_replies_toggle" href="/MarsWxReport/with_replies">
                    Tweets &amp; replies
                   </a>
                  </li>
                  <li class="ProfileHeading-toggleItem u-textUserColor" data-element-term="photos_and_videos_toggle">
                   <a class="ProfileHeading-toggleLink js-openSignupDialog js-nonNavigable" data-nav="photos_and_videos_toggle" href="/MarsWxReport/media">
                    Media
                   </a>
                  </li>
                 </ul>
                </div>
               </div>
               <div class="ProfileWarningTimeline" data-element-context="blocked_profile">
                <h2 class="ProfileWarningTimeline-heading" id="content-main-heading">
                 You blocked
                 <span class="username u-dir u-textTruncate" dir="ltr">
                  @
                  <b>
                   MarsWxReport
                  </b>
                 </span>
                </h2>
                <p class="ProfileWarningTimeline-explanation">
                 Are you sure you want to view these Tweets? Viewing Tweets won't unblock
                 <span class="username u-dir u-textTruncate" dir="ltr">
                  @
                  <b>
                   MarsWxReport
                  </b>
                 </span>
                </p>
                <button class="EdgeButton EdgeButton--tertiary ProfileWarningTimeline-button">
                 Yes, view profile
                </button>
               </div>
               <div class="ScrollBumpDialog modal-container" id="scroll-bump-dialog">
                <div class="modal draggable">
                 <div class="modal-content clearfix">
                  <button class="modal-btn modal-close js-close" type="button">
                   <span class="Icon Icon--close Icon--medium">
                    <span class="visuallyhidden">
                     Close
                    </span>
                   </span>
                  </button>
                  <div class="modal-header">
                   <h3 class="modal-title">
                    Mars Weather followed
                   </h3>
                  </div>
                  <div class="modal-body">
                   <div class="loading">
                    <span class="spinner-bigger">
                    </span>
                   </div>
                   <ol class="ScrollBumpDialog-usersList clearfix js-users-list">
                   </ol>
                  </div>
                 </div>
                </div>
               </div>
               <div class="ProfileTimeline " id="timeline">
                <div class="stream-container " data-max-position="1019403188766691328" data-min-position="1012127708917194752">
                 <div class="stream-item js-new-items-bar-container">
                 </div>
                 <div class="stream">
                  <ol class="stream-items js-navigable-stream" id="stream-items-id">
                   <li class="js-stream-item stream-item stream-item " data-item-id="1019223008492187648" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1019223008492187648","scribe_component":"tweet"}' id="stream-item-tweet-1019223008492187648">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet tweet-has-context " data-conversation-id="1019223008492187648" data-disclosure-type="" data-follows-you="false" data-item-id="1019223008492187648" data-name="Allen Chen" data-permalink-path="/icancallubetty/status/1019223008492187648" data-reply-to-users-json='[{"id_str":"81934163","screen_name":"icancallubetty","name":"Allen Chen","emojified_name":{"text":"Allen Chen","emojified_text_as_html":"Allen Chen"}},{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-retweet-id="1019403188766691328" data-retweeter="MarsWxReport" data-screen-name="icancallubetty" data-tweet-id="1019223008492187648" data-tweet-nonce="1019223008492187648-bd7f1b2c-4ded-408e-82ad-a30969f23a59" data-tweet-stat-initialized="true" data-user-id="81934163" data-you-block="false" data-you-follow="false">
                     <div class="context">
                      <div class="tweet-context with-icn ">
                       <span class="Icon Icon--small Icon--retweeted">
                       </span>
                       <span class="js-retweet-text">
                        <a class="pretty-link js-user-profile-link" data-user-id="786939553" href="/MarsWxReport" rel="noopener">
                         <b>
                          Mars Weather
                         </b>
                        </a>
                        Retweeted
                       </span>
                      </div>
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="81934163" href="/icancallubetty">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2482449328/6iogc6qso8wox0dlvsbo_bigger.png"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Allen Chen
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          icancallubetty
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1019223008492187648" href="/icancallubetty/status/1019223008492187648" title="7:11 AM - 17 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531836676" data-time-ms="1531836676000">
                          Jul 17
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        L-2 years.
                        <a class="twitter-hashtag pretty-link js-nav" data-query-source="hashtag_click" dir="ltr" href="/hashtag/Mars2020?src=hash">
                         <s>
                          #
                         </s>
                         <b>
                          Mars2020
                         </b>
                        </a>
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="2">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1019223008492187648">
                           2 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="6">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1019223008492187648">
                           6 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="25">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1019223008492187648">
                           25 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1019223008492187648" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            2
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1019223008492187648" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1019223008492187648" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            25
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            25
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1017925917065302016" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1017925917065302016","scribe_component":"tweet"}' id="stream-item-tweet-1017925917065302016">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1017925917065302016" data-disclosure-type="" data-follows-you="false" data-item-id="1017925917065302016" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1017925917065302016" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1017925917065302016" data-tweet-nonce="1017925917065302016-dc2719c7-bcea-466c-af67-23153e713678" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1017925917065302016" href="/MarsWxReport/status/1017925917065302016" title="5:17 PM - 13 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531527425" data-time-ms="1531527425000">
                          Jul 13
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2108 (2018-07-12), Sunny, high -24C/-11F, low -65C/-84F, pressure at 8.06 hPa, daylight 05:19-17:27
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1017925917065302016">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="7">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1017925917065302016">
                           7 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="15">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1017925917065302016">
                           15 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1017925917065302016" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1017925917065302016" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1017925917065302016" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1017563527509434374" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1017563527509434374","scribe_component":"tweet"}' id="stream-item-tweet-1017563527509434374">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1017563527509434374" data-disclosure-type="" data-follows-you="false" data-item-id="1017563527509434374" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1017563527509434374" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1017563527509434374" data-tweet-nonce="1017563527509434374-096c43b7-f352-48ed-b37f-8da3bc10869b" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1017563527509434374" href="/MarsWxReport/status/1017563527509434374" title="5:17 PM - 12 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531441025" data-time-ms="1531441025000">
                          Jul 12
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2107 (2018-07-11), Sunny, high -21C/-5F, low -65C/-84F, pressure at 8.07 hPa, daylight 05:19-17:27
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1017563527509434374">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="8">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1017563527509434374">
                           8 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="12">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1017563527509434374">
                           12 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1017563527509434374" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1017563527509434374" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            8
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            8
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1017563527509434374" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            12
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            12
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1017201141568942080" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1017201141568942080","scribe_component":"tweet"}' id="stream-item-tweet-1017201141568942080">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1017201141568942080" data-disclosure-type="" data-follows-you="false" data-item-id="1017201141568942080" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1017201141568942080" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1017201141568942080" data-tweet-nonce="1017201141568942080-15d6bd7f-b098-423d-b252-99716bd25163" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1017201141568942080" href="/MarsWxReport/status/1017201141568942080" title="5:17 PM - 11 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531354625" data-time-ms="1531354625000">
                          Jul 11
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2106 (2018-07-09), Sunny, high -27C/-16F, low -59C/-74F, pressure at 8.06 hPa, daylight 05:19-17:26
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1017201141568942080">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="9">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1017201141568942080">
                           9 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="22">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1017201141568942080">
                           22 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1017201141568942080" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1017201141568942080" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            9
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            9
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1017201141568942080" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            22
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            22
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1017201140298059778" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1017201140298059778","scribe_component":"tweet"}' id="stream-item-tweet-1017201140298059778">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1017201140298059778" data-disclosure-type="" data-follows-you="false" data-item-id="1017201140298059778" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1017201140298059778" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1017201140298059778" data-tweet-nonce="1017201140298059778-ed38f2d6-79af-4453-a719-8cde09dcfe91" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1017201140298059778" href="/MarsWxReport/status/1017201140298059778" title="5:17 PM - 11 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531354625" data-time-ms="1531354625000">
                          Jul 11
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2105 (2018-07-08), Sunny, high -25C/-12F, low -61C/-77F, pressure at 8.02 hPa, daylight 05:18-17:26
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1017201140298059778">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="3">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1017201140298059778">
                           3 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="14">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1017201140298059778">
                           14 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1017201140298059778" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1017201140298059778" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1017201140298059778" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            14
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            14
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1016476366546571264" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1016476366546571264","scribe_component":"tweet"}' id="stream-item-tweet-1016476366546571264">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1016476366546571264" data-disclosure-type="" data-follows-you="false" data-item-id="1016476366546571264" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1016476366546571264" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1016476366546571264" data-tweet-nonce="1016476366546571264-4048ae48-2185-434e-9607-1b5606ba5087" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1016476366546571264" href="/MarsWxReport/status/1016476366546571264" title="5:17 PM - 9 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531181825" data-time-ms="1531181825000">
                          Jul 9
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2104 (2018-07-07), Sunny, high -23C/-9F, low -59C/-74F, pressure at 7.97 hPa, daylight 05:18-17:26
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1016476366546571264">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="9">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1016476366546571264">
                           9 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="16">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1016476366546571264">
                           16 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1016476366546571264" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1016476366546571264" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            9
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            9
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1016476366546571264" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            16
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            16
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1016476365418389504" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1016476365418389504","scribe_component":"tweet"}' id="stream-item-tweet-1016476365418389504">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1016476365418389504" data-disclosure-type="" data-follows-you="false" data-item-id="1016476365418389504" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1016476365418389504" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1016476365418389504" data-tweet-nonce="1016476365418389504-3fd28088-7f8d-454c-839d-18139023a6c1" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1016476365418389504" href="/MarsWxReport/status/1016476365418389504" title="5:17 PM - 9 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531181825" data-time-ms="1531181825000">
                          Jul 9
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2103 (2018-07-06), Sunny, high -26C/-14F, low -58C/-72F, pressure at 7.97 hPa, daylight 05:18-17:26
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1016476365418389504">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="4">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1016476365418389504">
                           4 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="8">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1016476365418389504">
                           8 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1016476365418389504" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1016476365418389504" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            4
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            4
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1016476365418389504" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            8
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            8
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1016476364264951808" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1016476364264951808","scribe_component":"tweet"}' id="stream-item-tweet-1016476364264951808">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1016476364264951808" data-disclosure-type="" data-follows-you="false" data-item-id="1016476364264951808" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1016476364264951808" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1016476364264951808" data-tweet-nonce="1016476364264951808-2da1cff0-26da-4720-9f26-a24215655dbf" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1016476364264951808" href="/MarsWxReport/status/1016476364264951808" title="5:17 PM - 9 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531181825" data-time-ms="1531181825000">
                          Jul 9
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2102 (2018-07-05), Sunny, high -22C/-7F, low -60C/-75F, pressure at 7.97 hPa, daylight 05:18-17:25
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1016476364264951808">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="2">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1016476364264951808">
                           2 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="8">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1016476364264951808">
                           8 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1016476364264951808" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1016476364264951808" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            2
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            2
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1016476364264951808" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            8
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            8
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1016476363308625921" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1016476363308625921","scribe_component":"tweet"}' id="stream-item-tweet-1016476363308625921">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1016476363308625921" data-disclosure-type="" data-follows-you="false" data-item-id="1016476363308625921" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1016476363308625921" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1016476363308625921" data-tweet-nonce="1016476363308625921-b05accc0-4e14-4cb8-9940-48ae66489f75" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1016476363308625921" href="/MarsWxReport/status/1016476363308625921" title="5:17 PM - 9 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1531181824" data-time-ms="1531181824000">
                          Jul 9
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2101 (2018-07-04), Sunny, high -23C/-9F, low -61C/-77F, pressure at 7.96 hPa, daylight 05:18-17:25
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1016476363308625921">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="4">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1016476363308625921">
                           4 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="10">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1016476363308625921">
                           10 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1016476363308625921" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1016476363308625921" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            4
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            4
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1016476363308625921" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            10
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            10
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1015389200127086592" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1015389200127086592","scribe_component":"tweet"}' id="stream-item-tweet-1015389200127086592">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1015389200127086592" data-disclosure-type="" data-follows-you="false" data-item-id="1015389200127086592" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1015389200127086592" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1015389200127086592" data-tweet-nonce="1015389200127086592-b7458871-4ccd-4281-899d-a554b3efde94" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1015389200127086592" href="/MarsWxReport/status/1015389200127086592" title="5:17 PM - 6 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530922624" data-time-ms="1530922624000">
                          Jul 6
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2100 (2018-07-03), Sunny, high -29C/-20F, low -61C/-77F, pressure at 7.97 hPa, daylight 05:18-17:25
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1015389200127086592">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="7">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1015389200127086592">
                           7 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="15">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1015389200127086592">
                           15 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1015389200127086592" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1015389200127086592" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1015389200127086592" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1014664425486409734" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1014664425486409734","scribe_component":"tweet"}' id="stream-item-tweet-1014664425486409734">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1014664425486409734" data-disclosure-type="" data-follows-you="false" data-item-id="1014664425486409734" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1014664425486409734" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1014664425486409734" data-tweet-nonce="1014664425486409734-c0dfe27a-7862-40cc-8661-80bb6f9779c3" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1014664425486409734" href="/MarsWxReport/status/1014664425486409734" title="5:17 PM - 4 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530749825" data-time-ms="1530749825000">
                          Jul 4
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2099 (2018-07-02), Sunny, high -25C/-12F, low -61C/-77F, pressure at 7.91 hPa, daylight 05:18-17:25
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1014664425486409734">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="6">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1014664425486409734">
                           6 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="15">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1014664425486409734">
                           15 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1014664425486409734" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1014664425486409734" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1014664425486409734" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1014598800860516352" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1014598800860516352","scribe_component":"tweet"}' id="stream-item-tweet-1014598800860516352">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet tweet-has-context has-cards has-content " data-conversation-id="1014598800860516352" data-disclosure-type="" data-follows-you="false" data-has-cards="true" data-item-id="1014598800860516352" data-name="Doug Ellison" data-permalink-path="/doug_ellison/status/1014598800860516352" data-reply-to-users-json='[{"id_str":"15402623","screen_name":"doug_ellison","name":"Doug Ellison","emojified_name":{"text":"Doug Ellison","emojified_text_as_html":"Doug Ellison"}},{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-retweet-id="1014615140455600128" data-retweeter="MarsWxReport" data-screen-name="doug_ellison" data-tweet-id="1014598800860516352" data-tweet-nonce="1014598800860516352-24953ae3-2f6f-4d4b-8869-81e9aa887ab9" data-tweet-stat-initialized="true" data-user-id="15402623" data-you-block="false" data-you-follow="false">
                     <div class="context">
                      <div class="tweet-context with-icn ">
                       <span class="Icon Icon--small Icon--retweeted">
                       </span>
                       <span class="js-retweet-text">
                        <a class="pretty-link js-user-profile-link" data-user-id="786939553" href="/MarsWxReport" rel="noopener">
                         <b>
                          Mars Weather
                         </b>
                        </a>
                        Retweeted
                       </span>
                      </div>
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="15402623" href="/doug_ellison">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/906197548771172352/bBSBKKAB_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Doug Ellison
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          doug_ellison
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1014598800860516352" href="/doug_ellison/status/1014598800860516352" title="12:56 PM - 4 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530734179" data-time-ms="1530734179000">
                          Jul 4
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Happy 21st Birthday, Pathfinder And Sojourner
                        <a class="twitter-timeline-link u-hidden" data-pre-embedded="true" dir="ltr" href="https://t.co/lhCOwq09Rt">
                         pic.twitter.com/lhCOwq09Rt
                        </a>
                       </p>
                      </div>
                      <div class="AdaptiveMediaOuterContainer">
                       <div class="AdaptiveMedia is-square ">
                        <div class="AdaptiveMedia-container">
                         <div class="AdaptiveMedia-singlePhoto" style="padding-top: calc(0.7255859375 * 100% - 0.5px);">
                          <div class="AdaptiveMedia-photoContainer js-adaptive-photo " data-dominant-color="[64,56,54]" data-element-context="platform_photo_card" data-image-url="https://pbs.twimg.com/media/DhSUOsLUYAUHena.jpg" style="background-color:rgba(64,56,54,1.0);">
                           <img alt="" data-aria-label-part="" src="https://pbs.twimg.com/media/DhSUOsLUYAUHena.jpg" style="width: 100%; top: -0px;"/>
                          </div>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="4">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1014598800860516352">
                           4 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="68">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1014598800860516352">
                           68 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="187">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1014598800860516352">
                           187 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1014598800860516352" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            4
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1014598800860516352" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            68
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            68
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1014598800860516352" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            187
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            187
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1014302036232372224" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1014302036232372224","scribe_component":"tweet"}' id="stream-item-tweet-1014302036232372224">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1014302036232372224" data-disclosure-type="" data-follows-you="false" data-item-id="1014302036232372224" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1014302036232372224" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1014302036232372224" data-tweet-nonce="1014302036232372224-4720a84c-4343-4e79-a736-47463e1868dd" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1014302036232372224" href="/MarsWxReport/status/1014302036232372224" title="5:17 PM - 3 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530663424" data-time-ms="1530663424000">
                          Jul 3
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2098 (2018-07-01), Sunny, high -23C/-9F, low -61C/-77F, pressure at 7.91 hPa, daylight 05:18-17:24
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="3">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1014302036232372224">
                           3 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="7">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1014302036232372224">
                           7 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="15">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1014302036232372224">
                           15 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1014302036232372224" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1014302036232372224" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1014302036232372224" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1013939650354995200" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1013939650354995200","scribe_component":"tweet"}' id="stream-item-tweet-1013939650354995200">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1013939650354995200" data-disclosure-type="" data-follows-you="false" data-item-id="1013939650354995200" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1013939650354995200" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1013939650354995200" data-tweet-nonce="1013939650354995200-a32ad5a3-72d6-4a21-b4fe-d9852a05ba31" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1013939650354995200" href="/MarsWxReport/status/1013939650354995200" title="5:17 PM - 2 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530577025" data-time-ms="1530577025000">
                          Jul 2
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2097 (2018-06-30), Sunny, high -23C/-9F, low -60C/-75F, pressure at 7.89 hPa, daylight 05:18-17:24
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1013939650354995200">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="7">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1013939650354995200">
                           7 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="15">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1013939650354995200">
                           15 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1013939650354995200" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1013939650354995200" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1013939650354995200" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            15
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1013939649335701509" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1013939649335701509","scribe_component":"tweet"}' id="stream-item-tweet-1013939649335701509">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1013939649335701509" data-disclosure-type="" data-follows-you="false" data-item-id="1013939649335701509" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1013939649335701509" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1013939649335701509" data-tweet-nonce="1013939649335701509-7452b8e8-a9fa-4ad5-897a-1d71c96df7e9" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1013939649335701509" href="/MarsWxReport/status/1013939649335701509" title="5:17 PM - 2 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530577025" data-time-ms="1530577025000">
                          Jul 2
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2096 (2018-06-29), Sunny, high -22C/-7F, low -63C/-81F, pressure at 7.88 hPa, daylight 05:18-17:24
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1013939649335701509">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="5">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1013939649335701509">
                           5 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="9">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1013939649335701509">
                           9 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1013939649335701509" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1013939649335701509" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            5
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            5
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1013939649335701509" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            9
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            9
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1013939648471732224" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1013939648471732224","scribe_component":"tweet"}' id="stream-item-tweet-1013939648471732224">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1013939648471732224" data-disclosure-type="" data-follows-you="false" data-item-id="1013939648471732224" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1013939648471732224" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1013939648471732224" data-tweet-nonce="1013939648471732224-47584f11-90a0-4cd6-a236-c0935ed626f8" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1013939648471732224" href="/MarsWxReport/status/1013939648471732224" title="5:17 PM - 2 Jul 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530577024" data-time-ms="1530577024000">
                          Jul 2
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2095 (2018-06-28), Sunny, high -25C/-12F, low -61C/-77F, pressure at 7.84 hPa, daylight 05:18-17:24
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1013939648471732224">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="3">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1013939648471732224">
                           3 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="7">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1013939648471732224">
                           7 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1013939648471732224" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1013939648471732224" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1013939648471732224" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1012852487202770945" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1012852487202770945","scribe_component":"tweet"}' id="stream-item-tweet-1012852487202770945">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1012852487202770945" data-disclosure-type="" data-follows-you="false" data-item-id="1012852487202770945" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1012852487202770945" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1012852487202770945" data-tweet-nonce="1012852487202770945-d35f65a8-5b1d-461d-a493-f1e5cecf127e" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1012852487202770945" href="/MarsWxReport/status/1012852487202770945" title="5:17 PM - 29 Jun 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530317825" data-time-ms="1530317825000">
                          Jun 29
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2094 (2018-06-27), Sunny, high -27C/-16F, low -61C/-77F, pressure at 7.83 hPa, daylight 05:18-17:24
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="1">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1012852487202770945">
                           1 reply
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="6">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1012852487202770945">
                           6 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="10">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1012852487202770945">
                           10 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1012852487202770945" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            1
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1012852487202770945" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1012852487202770945" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            10
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            10
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1012852486049353730" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1012852486049353730","scribe_component":"tweet"}' id="stream-item-tweet-1012852486049353730">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1012852486049353730" data-disclosure-type="" data-follows-you="false" data-item-id="1012852486049353730" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1012852486049353730" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1012852486049353730" data-tweet-nonce="1012852486049353730-51997f0c-011e-460f-8615-0e014f6e19d9" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1012852486049353730" href="/MarsWxReport/status/1012852486049353730" title="5:17 PM - 29 Jun 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530317825" data-time-ms="1530317825000">
                          Jun 29
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2093 (2018-06-26), Sunny, high -24C/-11F, low -63C/-81F, pressure at 7.80 hPa, daylight 05:18-17:23
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1012852486049353730">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="3">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1012852486049353730">
                           3 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="6">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1012852486049353730">
                           6 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1012852486049353730" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1012852486049353730" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1012852486049353730" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            6
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1012127710443909122" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1012127710443909122","scribe_component":"tweet"}' id="stream-item-tweet-1012127710443909122">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1012127710443909122" data-disclosure-type="" data-follows-you="false" data-item-id="1012127710443909122" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1012127710443909122" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1012127710443909122" data-tweet-nonce="1012127710443909122-27bc56bb-bd5e-41f7-8729-a235f760233a" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1012127710443909122" href="/MarsWxReport/status/1012127710443909122" title="5:17 PM - 27 Jun 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530145025" data-time-ms="1530145025000">
                          Jun 27
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2092 (2018-06-25), Sunny, high -24C/-11F, low -67C/-88F, pressure at 7.81 hPa, daylight 05:18-17:23
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="3">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-reply-count-aria-1012127710443909122">
                           3 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="7">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1012127710443909122">
                           7 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="18">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1012127710443909122">
                           18 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1012127710443909122" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1012127710443909122" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            7
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1012127710443909122" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            18
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            18
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                   <li class="js-stream-item stream-item stream-item " data-item-id="1012127708917194752" data-item-type="tweet" data-suggestion-json='{"suggestion_details":{},"tweet_ids":"1012127708917194752","scribe_component":"tweet"}' id="stream-item-tweet-1012127708917194752">
                    <div class="tweet js-stream-tweet js-actionable-tweet js-profile-popup-actionable dismissible-content original-tweet js-original-tweet " data-conversation-id="1012127708917194752" data-disclosure-type="" data-follows-you="false" data-item-id="1012127708917194752" data-name="Mars Weather" data-permalink-path="/MarsWxReport/status/1012127708917194752" data-reply-to-users-json='[{"id_str":"786939553","screen_name":"MarsWxReport","name":"Mars Weather","emojified_name":{"text":"Mars Weather","emojified_text_as_html":"Mars Weather"}}]' data-screen-name="MarsWxReport" data-tweet-id="1012127708917194752" data-tweet-nonce="1012127708917194752-27b1321b-6d28-4347-9417-bb818a036e84" data-tweet-stat-initialized="true" data-user-id="786939553" data-you-block="false" data-you-follow="false">
                     <div class="context">
                     </div>
                     <div class="content">
                      <div class="stream-item-header">
                       <a class="account-group js-account-group js-action-profile js-user-profile-link js-nav" data-user-id="786939553" href="/MarsWxReport">
                        <img alt="" class="avatar js-action-profile-avatar" src="https://pbs.twimg.com/profile_images/2552209293/220px-Mars_atmosphere_bigger.jpg"/>
                        <span class="FullNameGroup">
                         <strong class="fullname show-popup-with-id u-textTruncate " data-aria-label-part="">
                          Mars Weather
                         </strong>
                         <span>
                          ‏
                         </span>
                         <span class="UserBadges">
                         </span>
                         <span class="UserNameBreak">
                         </span>
                        </span>
                        <span class="username u-dir u-textTruncate" data-aria-label-part="" dir="ltr">
                         @
                         <b>
                          MarsWxReport
                         </b>
                        </span>
                       </a>
                       <small class="time">
                        <a class="tweet-timestamp js-permalink js-nav js-tooltip" data-conversation-id="1012127708917194752" href="/MarsWxReport/status/1012127708917194752" title="5:17 PM - 27 Jun 2018">
                         <span class="_timestamp js-short-timestamp " data-aria-label-part="last" data-long-form="true" data-time="1530145024" data-time-ms="1530145024000">
                          Jun 27
                         </span>
                        </a>
                       </small>
                       <div class="ProfileTweet-action ProfileTweet-action--more js-more-ProfileTweet-actions">
                        <div class="dropdown">
                         <button class="ProfileTweet-actionButton u-textUserColorHover dropdown-toggle js-dropdown-toggle" type="button">
                          <div class="IconContainer js-tooltip" title="More">
                           <span class="Icon Icon--caretDownLight Icon--small">
                           </span>
                           <span class="u-hiddenVisually">
                            More
                           </span>
                          </div>
                         </button>
                         <div class="dropdown-menu is-autoCentered">
                          <div class="dropdown-caret">
                           <div class="caret-outer">
                           </div>
                           <div class="caret-inner">
                           </div>
                          </div>
                          <ul>
                           <li class="copy-link-to-tweet js-actionCopyLinkToTweet">
                            <button class="dropdown-link" type="button">
                             Copy link to Tweet
                            </button>
                           </li>
                           <li class="embed-link js-actionEmbedTweet" data-nav="embed_tweet">
                            <button class="dropdown-link" type="button">
                             Embed Tweet
                            </button>
                           </li>
                          </ul>
                         </div>
                        </div>
                       </div>
                      </div>
                      <div class="js-tweet-text-container">
                       <p class="TweetTextSize TweetTextSize--normal js-tweet-text tweet-text" data-aria-label-part="0" lang="en">
                        Sol 2091 (2018-06-24), Sunny, high -22C/-7F, low -63C/-81F, pressure at 7.79 hPa, daylight 05:18-17:23
                       </p>
                      </div>
                      <div class="stream-item-footer">
                       <div class="ProfileTweet-actionCountList u-hiddenVisually">
                        <span class="ProfileTweet-action--reply u-hiddenVisually">
                         <span aria-hidden="true" class="ProfileTweet-actionCount" data-tweet-stat-count="0">
                          <span class="ProfileTweet-actionCountForAria" id="profile-tweet-action-reply-count-aria-1012127708917194752">
                           0 replies
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--retweet u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="3">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-retweet-count-aria-1012127708917194752">
                           3 retweets
                          </span>
                         </span>
                        </span>
                        <span class="ProfileTweet-action--favorite u-hiddenVisually">
                         <span class="ProfileTweet-actionCount" data-tweet-stat-count="12">
                          <span class="ProfileTweet-actionCountForAria" data-aria-label-part="" id="profile-tweet-action-favorite-count-aria-1012127708917194752">
                           12 likes
                          </span>
                         </span>
                        </span>
                       </div>
                       <div aria-label="Tweet actions" class="ProfileTweet-actionList js-actions" role="group">
                        <div class="ProfileTweet-action ProfileTweet-action--reply">
                         <button aria-describedby="profile-tweet-action-reply-count-aria-1012127708917194752" class="ProfileTweet-actionButton js-actionButton js-actionReply" data-modal="ProfileTweet-reply" type="button">
                          <div class="IconContainer js-tooltip" title="Reply">
                           <span class="Icon Icon--medium Icon--reply">
                           </span>
                           <span class="u-hiddenVisually">
                            Reply
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount ProfileTweet-actionCount--isZero ">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--retweet js-toggleState js-toggleRt">
                         <button aria-describedby="profile-tweet-action-retweet-count-aria-1012127708917194752" class="ProfileTweet-actionButton js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweet
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo js-actionButton js-actionRetweet" data-modal="ProfileTweet-retweet" type="button">
                          <div class="IconContainer js-tooltip" title="Undo retweet">
                           <span class="Icon Icon--medium Icon--retweet">
                           </span>
                           <span class="u-hiddenVisually">
                            Retweeted
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            3
                           </span>
                          </span>
                         </button>
                        </div>
                        <div class="ProfileTweet-action ProfileTweet-action--favorite js-toggleState">
                         <button aria-describedby="profile-tweet-action-favorite-count-aria-1012127708917194752" class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Like
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            12
                           </span>
                          </span>
                         </button>
                         <button class="ProfileTweet-actionButtonUndo ProfileTweet-action--unfavorite u-linkClean js-actionButton js-actionFavorite" type="button">
                          <div class="IconContainer js-tooltip" title="Undo like">
                           <span class="Icon Icon--heart Icon--medium" role="presentation">
                           </span>
                           <div class="HeartAnimation">
                           </div>
                           <span class="u-hiddenVisually">
                            Liked
                           </span>
                          </div>
                          <span class="ProfileTweet-actionCount">
                           <span aria-hidden="true" class="ProfileTweet-actionCountForPresentation">
                            12
                           </span>
                          </span>
                         </button>
                        </div>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="dismiss-module">
                     <div class="dismissed-module">
                      <div class="feedback-actions">
                       <div class="feedback-action" data-feedback-type="DontLike" data-feedback-url="">
                        <div class="action-confirmation dismiss-module-item">
                         Thanks. Twitter will use this to make your timeline better.
                         <span class="undo-action">
                          Undo
                         </span>
                        </div>
                       </div>
                      </div>
                      <div class="child-feedback-confirmation">
                       <div class="child-confirmation-item">
                        <span class="child-confirmation-text">
                        </span>
                        <span class="undo-child-feedback-action">
                         Undo
                        </span>
                       </div>
                      </div>
                     </div>
                    </div>
                   </li>
                  </ol>
                  <div class="stream-footer ">
                   <div class="timeline-end has-items has-more-items">
                    <div class="stream-end">
                     <div class="stream-end-inner">
                      <span class="Icon Icon--large Icon--logo">
                      </span>
                      <p class="empty-text">
                       @MarsWxReport hasn't Tweeted yet.
                      </p>
                      <p>
                       <button class="btn-link back-to-top hidden" type="button">
                        Back to top ↑
                       </button>
                      </p>
                     </div>
                    </div>
                    <div class="stream-loading">
                     <div class="stream-end-inner">
                      <span class="spinner" title="Loading...">
                      </span>
                     </div>
                    </div>
                   </div>
                  </div>
                  <div class="stream-fail-container">
                   <div class="js-stream-whale-end stream-whale-end stream-placeholder centered-placeholder">
                    <div class="stream-end-inner">
                     <h2 class="title">
                      Loading seems to be taking a while.
                     </h2>
                     <p>
                      Twitter may be over capacity or experiencing a momentary hiccup.
                      <a class="try-again-after-whale" href="#" role="button">
                       Try again
                      </a>
                      or visit
                      <a href="http://status.twitter.com" rel="noopener" target="_blank">
                       Twitter Status
                      </a>
                      for more information.
                     </p>
                    </div>
                   </div>
                  </div>
                  <ol class="hidden-replies-container">
                  </ol>
                 </div>
                </div>
               </div>
              </div>
              <div class="Grid-cell u-size1of3">
               <div class="Grid Grid--withGutter">
                <div class="Grid-cell">
                 <div class="ProfileSidebar ProfileSidebar--withRightAlignment">
                  <div class="MoveableModule">
                   <div class="SidebarCommonModules">
                    <div class="SignupCallOut module js-signup-call-out ">
                     <div class="SignupCallOut-header">
                      <h3 class="SignupCallOut-title u-textBreak">
                       New to Twitter?
                      </h3>
                     </div>
                     <div class="SignupCallOut-subheader">
                      Sign up now to get your own personalized timeline!
                     </div>
                     <div class="signup SignupForm ">
                      <a class="EdgeButton EdgeButton--large EdgeButton--primary SignupForm-submit u-block js-signup " data-component="signup_callout" data-element="form" href="https://twitter.com/signup" role="button">
                       Sign up
                      </a>
                     </div>
                    </div>
                    <div class="RelatedUsers module u-hidden">
                     <div class="RelatedUsers-header">
                      <h3 class="RelatedUsers-title">
                       You may also like
                      </h3>
                      ·
                      <button class="btn-link js-refresh-related-users" type="button">
                       Refresh
                      </button>
                     </div>
                     <div class="RelatedUsers-users">
                     </div>
                    </div>
                    <div class="module Trends trends hidden">
                     <div class="trends-inner">
                      <div class="flex-module trends-container ">
                       <div class="flex-module-header">
                        <h3>
                         <span class="trend-location js-trend-location">
                          false
                         </span>
                        </h3>
                       </div>
                       <div class="flex-module-inner">
                        <ul class="trend-items js-trends">
                        </ul>
                       </div>
                      </div>
                     </div>
                    </div>
                    <div class="Footer module roaming-module Footer--slim Footer--blankBackground">
                     <div class="flex-module">
                      <div class="flex-module-inner js-items-container">
                       <ul class="u-cf">
                        <li class="Footer-item Footer-copyright copyright">
                         © 2018 Twitter
                        </li>
                        <li class="Footer-item">
                         <a class="Footer-link" href="/about" rel="noopener">
                          About
                         </a>
                        </li>
                        <li class="Footer-item">
                         <a class="Footer-link" href="//support.twitter.com" rel="noopener">
                          Help Center
                         </a>
                        </li>
                        <li class="Footer-item">
                         <a class="Footer-link" href="/tos" rel="noopener">
                          Terms
                         </a>
                        </li>
                        <li class="Footer-item">
                         <a class="Footer-link" href="/privacy" rel="noopener">
                          Privacy policy
                         </a>
                        </li>
                        <li class="Footer-item">
                         <a class="Footer-link" href="//support.twitter.com/articles/20170514" rel="noopener">
                          Cookies
                         </a>
                        </li>
                        <li class="Footer-item">
                         <a class="Footer-link" href="//support.twitter.com/articles/20170451" rel="noopener">
                          Ads info
                         </a>
                        </li>
                       </ul>
                      </div>
                     </div>
                    </div>
                   </div>
                  </div>
                 </div>
                </div>
               </div>
              </div>
             </div>
            </div>
           </div>
          </div>
         </div>
         <div class="trends-dialog modal-container" id="trends_dialog">
          <div class="modal draggable">
           <div class="modal-content">
            <button class="modal-btn modal-close js-close" type="button">
             <span class="Icon Icon--close Icon--medium">
              <span class="visuallyhidden">
               Close
              </span>
             </span>
            </button>
            <div class="modal-header">
             <h3 class="modal-title">
              Choose a trend location
             </h3>
            </div>
            <div class="modal-body">
             <div class="trends-dialog-error">
              <p>
              </p>
             </div>
             <div class="trends-wrapper" id="trends_dialog_content">
              <div class="loading">
               <span class="spinner-bigger">
               </span>
              </div>
             </div>
            </div>
           </div>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="alert-messages hidden" id="message-drawer">
       <div class="message ">
        <div class="message-inside">
         <span class="message-text">
         </span>
         <a class="Icon Icon--close Icon--medium dismiss" href="#" role="button">
          <span class="visuallyhidden">
           Dismiss
          </span>
         </a>
        </div>
       </div>
      </div>
      <div class="gallery-overlay">
      </div>
      <div class="Gallery with-tweet">
       <style class="Gallery-styles">
       </style>
       <div class="Gallery-closeTarget">
       </div>
       <div class="Gallery-content">
        <button class="modal-btn modal-close modal-close-fixed js-close" type="button">
         <span class="Icon Icon--close Icon--large">
          <span class="visuallyhidden">
           Close
          </span>
         </span>
        </button>
        <div class="Gallery-media">
        </div>
        <div class="GalleryNav GalleryNav--prev">
         <span class="GalleryNav-handle GalleryNav-handle--prev">
          <span class="Icon Icon--caretLeft Icon--large">
           <span class="u-hiddenVisually">
            Previous
           </span>
          </span>
         </span>
        </div>
        <div class="GalleryNav GalleryNav--next">
         <span class="GalleryNav-handle GalleryNav-handle--next">
          <span class="Icon Icon--caretRight Icon--large">
           <span class="u-hiddenVisually">
            Next
           </span>
          </span>
         </span>
        </div>
        <div class="GalleryTweet">
        </div>
       </div>
      </div>
      <div class="modal-overlay">
      </div>
      <div id="profile-hover-container">
      </div>
      <div class="modal-container" id="goto-user-dialog">
       <div class="modal modal-small draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Go to a person's profile
          </h3>
         </div>
         <div class="modal-body">
          <div class="modal-inner">
           <form class="t1-form goto-user-form">
            <input aria-label="User" class="input-block username-input" placeholder="Start typing a name to jump to a profile" type="text"/>
            <div class="dropdown-menu typeahead" role="listbox">
             <div aria-hidden="true" class="dropdown-caret">
              <div class="caret-outer">
              </div>
              <div class="caret-inner">
              </div>
             </div>
             <div class="dropdown-inner js-typeahead-results" role="presentation">
              <div class="typeahead-saved-searches" role="presentation">
               <h3 class="typeahead-category-title saved-searches-title" id="saved-searches-heading">
                Saved searches
               </h3>
               <ul class="typeahead-items saved-searches-list" role="presentation">
                <li class="typeahead-item typeahead-saved-search-item" role="presentation">
                 <span aria-hidden="true" class="Icon Icon--close">
                  <span class="visuallyhidden">
                   Remove
                  </span>
                 </span>
                 <a aria-describedby="saved-searches-heading" class="js-nav" data-ds="saved_search" data-query-source="" data-search-query="" href="" role="option" tabindex="-1">
                 </a>
                </li>
               </ul>
              </div>
              <ul class="typeahead-items typeahead-topics" role="presentation">
               <li class="typeahead-item typeahead-topic-item" role="presentation">
                <a class="js-nav" data-ds="topics" data-query-source="typeahead_click" data-search-query="" href="" role="option" tabindex="-1">
                </a>
               </li>
              </ul>
              <ul class="typeahead-items typeahead-accounts social-context js-typeahead-accounts" role="presentation">
               <li class="typeahead-item typeahead-account-item js-selectable" data-remote="true" data-score="" data-user-id="" data-user-screenname="" role="presentation">
                <a class="js-nav" data-ds="account" data-query-source="typeahead_click" data-search-query="" role="option">
                 <div class="js-selectable typeahead-in-conversation hidden">
                  <span class="Icon Icon--follower Icon--small">
                  </span>
                  <span class="typeahead-in-conversation-text">
                   In this conversation
                  </span>
                 </div>
                 <img alt="" class="avatar size32"/>
                 <span class="typeahead-user-item-info account-group">
                  <span class="fullname">
                  </span>
                  <span class="UserBadges">
                   <span class="Icon Icon--verified js-verified hidden">
                    <span class="u-hiddenVisually">
                     Verified account
                    </span>
                   </span>
                   <span class="Icon Icon--protected js-protected hidden">
                    <span class="u-hiddenVisually">
                     Protected Tweets
                    </span>
                   </span>
                  </span>
                  <span class="UserNameBreak">
                  </span>
                  <span class="username u-dir" dir="ltr">
                   @
                   <b>
                   </b>
                  </span>
                 </span>
                 <span class="typeahead-social-context">
                 </span>
                </a>
               </li>
               <li class="js-selectable typeahead-accounts-shortcut js-shortcut" role="presentation">
                <a class="js-nav" data-ds="account_search" data-query-source="typeahead_click" data-search-query="" data-shortcut="true" href="" role="option">
                </a>
               </li>
              </ul>
              <ul class="typeahead-items typeahead-trend-locations-list" role="presentation">
               <li class="typeahead-item typeahead-trend-locations-item" role="presentation">
                <a class="js-nav" data-ds="trend_location" data-search-query="" href="" role="option" tabindex="-1">
                </a>
               </li>
              </ul>
              <div class="typeahead-user-select" role="presentation">
               <div class="typeahead-empty-suggestions" role="presentation">
                Suggested users
               </div>
               <ul class="typeahead-items typeahead-selected js-typeahead-selected" role="presentation">
                <li class="typeahead-item typeahead-selected-item js-selectable" data-remote="true" data-score="" data-user-id="" data-user-screenname="" role="presentation">
                 <a class="js-nav" data-ds="account" data-query-source="typeahead_click" data-search-query="" role="option">
                  <img alt="" class="avatar size32"/>
                  <span class="typeahead-user-item-info account-group">
                   <span class="select-status deselect-user js-deselect-user Icon Icon--check">
                   </span>
                   <span class="select-status select-disabled Icon Icon--unfollow">
                   </span>
                   <span class="fullname">
                   </span>
                   <span class="UserBadges">
                    <span class="Icon Icon--verified js-verified hidden">
                     <span class="u-hiddenVisually">
                      Verified account
                     </span>
                    </span>
                    <span class="Icon Icon--protected js-protected hidden">
                     <span class="u-hiddenVisually">
                      Protected Tweets
                     </span>
                    </span>
                   </span>
                   <span class="UserNameBreak">
                   </span>
                   <span class="username u-dir" dir="ltr">
                    @
                    <b>
                    </b>
                   </span>
                  </span>
                 </a>
                </li>
                <li class="typeahead-selected-end" role="presentation">
                </li>
               </ul>
               <ul class="typeahead-items typeahead-accounts js-typeahead-accounts" role="presentation">
                <li class="typeahead-item typeahead-account-item js-selectable" data-remote="true" data-score="" data-user-id="" data-user-screenname="" role="presentation">
                 <a class="js-nav" data-ds="account" data-query-source="typeahead_click" data-search-query="" role="option">
                  <img alt="" class="avatar size32"/>
                  <span class="typeahead-user-item-info account-group">
                   <span class="select-status deselect-user js-deselect-user Icon Icon--check">
                   </span>
                   <span class="select-status select-disabled Icon Icon--unfollow">
                   </span>
                   <span class="fullname">
                   </span>
                   <span class="UserBadges">
                    <span class="Icon Icon--verified js-verified hidden">
                     <span class="u-hiddenVisually">
                      Verified account
                     </span>
                    </span>
                    <span class="Icon Icon--protected js-protected hidden">
                     <span class="u-hiddenVisually">
                      Protected Tweets
                     </span>
                    </span>
                   </span>
                   <span class="UserNameBreak">
                   </span>
                   <span class="username u-dir" dir="ltr">
                    @
                    <b>
                    </b>
                   </span>
                  </span>
                 </a>
                </li>
                <li class="typeahead-accounts-end" role="presentation">
                </li>
               </ul>
              </div>
              <div class="typeahead-dm-conversations" role="presentation">
               <ul class="typeahead-items typeahead-dm-conversation-items" role="presentation">
                <li class="typeahead-item typeahead-dm-conversation-item" role="presentation">
                 <a role="option" tabindex="-1">
                 </a>
                </li>
               </ul>
              </div>
             </div>
            </div>
           </form>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="QuickPromoteDialog modal-container" id="quick-promote-dialog">
       <div class="modal draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close modal-close-fixed js-close" type="button">
          <span class="Icon Icon--close Icon--large">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Promote this Tweet
          </h3>
         </div>
         <div class="modal-body">
          <div class="quick-promote-view-container">
           <div class="media">
            <iframe class="quick-promote-iframe js-initial-focus" frameborder="0" scrolling="no" src="">
            </iframe>
           </div>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="block-user-dialog">
       <div class="modal draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Block
          </h3>
         </div>
         <div class="tweet-loading">
          <div class="spinner-bigger">
          </div>
         </div>
         <div class="modal-body modal-tweet">
         </div>
         <div class="modal-footer">
          <button class="EdgeButton EdgeButton--tertiary cancel-action js-close">
           Cancel
          </button>
          <button class="EdgeButton EdgeButton--danger block-action">
           Block
          </button>
         </div>
        </div>
       </div>
      </div>
      <div id="geo-disabled-dropdown">
       <div tabindex="-1">
        <div class="dropdown-caret">
         <span class="caret-outer">
         </span>
         <span class="caret-inner">
         </span>
        </div>
        <ul>
         <li class="geo-not-enabled-yet">
          <h2>
           Tweet with a location
          </h2>
          <p>
           You can add location information to your Tweets, such as your city or precise location, from the web and via third-party applications. You always have the option to delete your Tweet location history.
           <a href="http://support.twitter.com/forums/26810/entries/78525" rel="noopener" target="_blank">
            Learn more
           </a>
          </p>
          <div>
           <button class="geo-turn-on EdgeButton EdgeButton--primary" type="button">
            Turn on
           </button>
           <button class="geo-not-now EdgeButton EdgeButton--secondary" type="button">
            Not now
           </button>
          </div>
         </li>
        </ul>
       </div>
      </div>
      <div id="geo-enabled-dropdown">
       <div tabindex="-1">
        <div class="dropdown-caret">
         <span class="caret-outer">
         </span>
         <span class="caret-inner">
         </span>
        </div>
        <div>
         <div class="geo-query-location">
          <input autocomplete="off" class="GeoSearch-queryInput" placeholder="Search for a neighborhood or city" type="text"/>
          <span class="Icon Icon--search">
          </span>
         </div>
         <div class="geo-dropdown-status">
         </div>
         <ul class="GeoSearch-dropdownMenu">
         </ul>
        </div>
       </div>
      </div>
      <div class="modal-container" id="list-membership-dialog">
       <div class="modal modal-small draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Your lists
          </h3>
         </div>
         <div class="modal-body">
          <div class="list-membership-content">
          </div>
          <span class="spinner lists-spinner" title="Loading…">
          </span>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="list-operations-dialog">
       <div class="modal modal-medium draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Create a new list
          </h3>
         </div>
         <div class="modal-body">
          <div class="list-editor">
           <div class="field">
            <label class="t1-label" for="list-name">
             List name
            </label>
            <input class="text" id="list-name" name="name" type="text" value="">
            </input>
           </div>
           <hr>
            <div class="field">
             <label class="t1-label" for="list-description">
              Description
             </label>
             <textarea id="list-description" name="description"></textarea>
             <span class="help-text">
              Under 100 characters, optional
             </span>
            </div>
            <hr/>
            <fieldset class="field">
             <legend class="t1-legend">
              Privacy
             </legend>
             <div class="options">
              <label class="t1-label" for="list-public-radio">
               <input checked="checked" class="radio" id="list-public-radio" name="mode" type="radio" value="public">
                <b>
                 Public
                </b>
                · Anyone can follow this list
               </input>
              </label>
              <label class="t1-label" for="list-private-radio">
               <input class="radio" id="list-private-radio" name="mode" type="radio" value="private">
                <b>
                 Private
                </b>
                · Only you can access this list
               </input>
              </label>
             </div>
            </fieldset>
            <hr/>
            <div class="list-editor-save">
             <button class="EdgeButton EdgeButton--secondary update-list-button" data-list-id="" type="button">
              Save list
             </button>
            </div>
           </hr>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="activity-popup-dialog">
       <div class="modal draggable">
        <div class="modal-content clearfix">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
          </h3>
         </div>
         <div class="modal-body">
          <div class="tweet-loading">
           <div class="spinner-bigger">
           </div>
          </div>
          <div class="activity-popup-dialog-content modal-tweet clearfix">
          </div>
          <div class="loading">
           <span class="spinner-bigger">
           </span>
          </div>
          <div class="activity-popup-dialog-users clearfix">
          </div>
          <div class="activity-popup-dialog-footer">
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="copy-link-to-tweet-dialog">
       <div class="modal modal-medium draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Copy link to Tweet
          </h3>
         </div>
         <div class="modal-body">
          <div class="copy-link-to-tweet-container">
           <label class="t1-label">
            <p class="copy-link-to-tweet-instructions">
             Here's the URL for this Tweet. Copy it to easily share with friends.
            </p>
            <textarea class="link-to-tweet-destination js-initial-focus u-dir" dir="ltr" readonly=""></textarea>
           </label>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="embed-tweet-dialog">
       <div class="modal modal-medium draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title embed-tweet-title">
           Embed this Tweet
          </h3>
          <h3 class="modal-title embed-video-title">
           Embed this Video
          </h3>
         </div>
         <div class="modal-body">
          <div class="embed-code-container">
           <p class="embed-tweet-instructions">
            Add this Tweet to your website by copying the code below.
            <a href="https://dev.twitter.com/web/embedded-tweets" rel="noopener" target="_blank">
             Learn more
            </a>
           </p>
           <p class="embed-video-instructions">
            Add this video to your website by copying the code below.
            <a href="https://dev.twitter.com/web/embedded-tweets" rel="noopener" target="_blank">
             Learn more
            </a>
           </p>
           <form class="t1-form">
            <div class="embed-destination-wrapper">
             <div class="embed-overlay embed-overlay-spinner">
              <div class="embed-overlay-content">
              </div>
             </div>
             <div class="embed-overlay embed-overlay-error">
              <p class="embed-overlay-content">
               Hmm, there was a problem reaching the server.
               <button class="btn-link retry-embed" type="button">
                Try again?
               </button>
              </p>
             </div>
             <textarea class="embed-destination js-initial-focus"></textarea>
             <div class="embed-options">
              <div class="embed-include-parent-tweet">
               <label class="t1-label" for="include-parent-tweet">
                <input checked="" class="include-parent-tweet" id="include-parent-tweet" type="checkbox"/>
                Include parent Tweet
               </label>
              </div>
              <div class="embed-include-card">
               <label class="t1-label" for="include-card">
                <input checked="" class="include-card" id="include-card" type="checkbox"/>
                Include media
               </label>
              </div>
             </div>
            </div>
           </form>
           <p class="embed-tweet-description">
            By embedding Twitter content in your website or app, you are agreeing to the Twitter
            <a href="https://dev.twitter.com/overview/terms/agreement" rel="noopener">
             Developer Agreement
            </a>
            and
            <a href="https://dev.twitter.com/overview/terms/policy" rel="noopener">
             Developer Policy
            </a>
            .
           </p>
           <h3 class="embed-preview-header">
            Preview
           </h3>
           <div class="embed-preview">
           </div>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container why-this-ad-dialog" id="why-this-ad-dialog">
       <div class="modal modal-large draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title why-this-ad-title">
           Why you're seeing this ad
          </h3>
         </div>
         <div class="why-this-ad-content">
          <div class="why-this-ad-spinner">
           <div class="spinner-bigger">
           </div>
          </div>
          <iframe aria-hidden="true" class="hidden" id="why-this-ad-frame" scrolling="auto">
          </iframe>
         </div>
        </div>
       </div>
      </div>
      <div class="LoginDialog modal-container u-textCenter" id="login-dialog">
       <div class="modal modal-large draggable">
        <div class="LoginDialog-content modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Log in to Twitter
          </h3>
         </div>
         <div class="LoginDialog-body modal-body">
          <div class="LoginDialog-bird">
           <span class="Icon Icon--bird Icon--large">
           </span>
          </div>
          <div class="LoginDialog-form">
           <form action="https://twitter.com/sessions" class="LoginForm js-front-signin" data-component="dialog" data-element="login" method="post">
            <div class="LoginForm-input LoginForm-username">
             <input autocomplete="username" class="text-input email-input js-signin-email" name="session[username_or_email]" placeholder="Phone, email, or username" type="text">
             </input>
            </div>
            <div class="LoginForm-input LoginForm-password">
             <input autocomplete="current-password" class="text-input" name="session[password]" placeholder="Password" type="password"/>
            </div>
            <div class="LoginForm-rememberForgot">
             <label>
              <input checked="checked" name="remember_me" type="checkbox" value="1"/>
              <span>
               Remember me
              </span>
             </label>
             <span class="separator">
              ·
             </span>
             <a class="forgot" href="/account/begin_password_reset" rel="noopener">
              Forgot password?
             </a>
            </div>
            <input class="EdgeButton EdgeButton--primary EdgeButton--medium submit js-submit" type="submit" value="Log in"/>
            <input name="return_to_ssl" type="hidden" value="true"/>
            <input name="scribe_log" type="hidden"/>
            <input name="redirect_after_login" type="hidden" value="/marswxreport?lang=en"/>
            <input name="authenticity_token" type="hidden" value="a1ca0d3455f25d81a0cd641472264bf8915226e3"/>
            <input autocomplete="off" name="ui_metrics" type="hidden"/>
            <script async="" src="/i/js_inst?c_name=ui_metrics">
            </script>
           </form>
          </div>
         </div>
         <div class="LoginDialog-footer modal-footer u-textCenter">
          Don't have an account?
          <a class="LoginDialog-signupLink" href="https://twitter.com/signup" rel="noopener">
           Sign up »
          </a>
         </div>
        </div>
       </div>
      </div>
      <div class="SignupDialog modal-container u-textCenter" id="signup-dialog">
       <div class="modal modal-large draggable">
        <div class="SignupDialog-content modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Sign up for Twitter
          </h3>
         </div>
         <div class="SignupDialog-body modal-body">
          <div class="SignupDialog-icon">
           <span class="Icon Icon--bird Icon--extraLarge">
           </span>
          </div>
          <h2 class="SignupDialog-heading">
           Not on Twitter? Sign up, tune into the things you care about, and get updates as they happen.
          </h2>
          <div class="SignupDialog-form">
           <div class="signup SignupForm ">
            <a class="EdgeButton EdgeButton--large EdgeButton--primary SignupForm-submit u-block js-signup " data-component="dialog" data-element="signup" href="https://twitter.com/signup" role="button">
             Sign up
            </a>
           </div>
          </div>
         </div>
         <div class="SignupDialog-footer modal-footer u-textCenter">
          Have an account?
          <a class="SignupDialog-signinLink" href="/login" rel="noopener">
           Log in »
          </a>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="sms-codes-dialog">
       <div class="modal modal-medium draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Two-way (sending and receiving) short codes:
          </h3>
         </div>
         <div class="modal-body">
          <table cellpadding="0" cellspacing="0" id="sms_codes">
           <thead>
            <tr>
             <th>
              Country
             </th>
             <th>
              Code
             </th>
             <th>
              For customers of
             </th>
            </tr>
           </thead>
           <tbody>
            <tr>
             <td>
              United States
             </td>
             <td>
              40404
             </td>
             <td>
              (any)
             </td>
            </tr>
            <tr>
             <td>
              Canada
             </td>
             <td>
              21212
             </td>
             <td>
              (any)
             </td>
            </tr>
            <tr>
             <td>
              United Kingdom
             </td>
             <td>
              86444
             </td>
             <td>
              Vodafone, Orange, 3, O2
             </td>
            </tr>
            <tr>
             <td>
              Brazil
             </td>
             <td>
              40404
             </td>
             <td>
              Nextel, TIM
             </td>
            </tr>
            <tr>
             <td>
              Haiti
             </td>
             <td>
              40404
             </td>
             <td>
              Digicel, Voila
             </td>
            </tr>
            <tr>
             <td>
              Ireland
             </td>
             <td>
              51210
             </td>
             <td>
              Vodafone, O2
             </td>
            </tr>
            <tr>
             <td>
              India
             </td>
             <td>
              53000
             </td>
             <td>
              Bharti Airtel, Videocon, Reliance
             </td>
            </tr>
            <tr>
             <td>
              Indonesia
             </td>
             <td>
              89887
             </td>
             <td>
              AXIS, 3, Telkomsel, Indosat, XL Axiata
             </td>
            </tr>
            <tr>
             <td rowspan="2">
              Italy
             </td>
             <td>
              4880804
             </td>
             <td>
              Wind
             </td>
            </tr>
            <tr>
             <td>
              3424486444
             </td>
             <td>
              Vodafone
             </td>
            </tr>
           </tbody>
           <tfoot>
            <tr>
             <td colspan="3">
              »
              <a class="js-initial-focus" href="http://support.twitter.com/articles/14226-how-to-find-your-twitter-short-code-or-long-code" rel="noopener" target="_blank">
               See SMS short codes for other countries
              </a>
             </td>
            </tr>
           </tfoot>
          </table>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="leadgen-confirm-dialog">
       <div class="modal draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close js-close" type="button">
          <span class="Icon Icon--close Icon--medium">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
           Confirmation
          </h3>
         </div>
         <div class="modal-body">
          <div class="leadgen-card-container">
           <div class="media">
            <iframe class="cards2-promotion-iframe" frameborder="0" scrolling="no" src="">
            </iframe>
           </div>
          </div>
          <div class="js-macaw-cards-iframe-container" data-card-name="promotion">
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="AuthWebViewDialog modal-container" id="auth-webview-dialog">
       <div class="modal draggable">
        <div class="modal-content">
         <button class="modal-btn modal-close modal-close-fixed js-close" type="button">
          <span class="Icon Icon--close Icon--large">
           <span class="visuallyhidden">
            Close
           </span>
          </span>
         </button>
         <div class="modal-header">
          <h3 class="modal-title">
          </h3>
         </div>
         <div class="modal-body">
          <div class="auth-webview-view-container">
           <div class="media">
            <iframe class="auth-webview-card-iframe js-initial-focus" frameborder="0" height="500px" scrolling="no" src="" width="590px">
            </iframe>
           </div>
          </div>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="promptbird-modal-prompt">
       <div class="modal">
        <button class="modal-btn js-promptDismiss modal-close js-close" type="button">
         <span class="Icon Icon--close Icon--medium">
          <span class="visuallyhidden">
           Close
          </span>
         </span>
        </button>
        <div class="modal-content">
        </div>
       </div>
      </div>
      <div class="modal-container UIWalkthrough" id="ui-walkthrough-dialog">
       <div class="UIWalkthrough-clickBlocker">
       </div>
       <div class="modal modal-small">
        <div class="UIWalkthrough-caret">
        </div>
        <div class="modal-content">
         <div class="modal-body">
          <div class="UIWalkthrough-header">
           <span class="UIWalkthrough-stepProgress">
           </span>
           <button class="UIWalkthrough-skip js-close">
            Skip all
           </button>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--welcome">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--home UIWalkthrough-icon">
            </span>
            Welcome home!
           </h3>
           <p class="UIWalkthrough-message">
            This timeline is where you’ll spend most of your time, getting instant updates about what matters to you.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--unfollow">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--smileRating1Fill UIWalkthrough-icon">
            </span>
            Tweets not working for you?
           </h3>
           <p class="UIWalkthrough-message">
            Hover over the profile pic and click the Following button to unfollow any account.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--like">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--heart UIWalkthrough-icon">
            </span>
            Say a lot with a little
           </h3>
           <p class="UIWalkthrough-message">
            When you see a Tweet you love, tap the heart — it lets  the person who wrote it know you shared the love.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--retweet">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--retweet UIWalkthrough-icon">
            </span>
            Spread the word
           </h3>
           <p class="UIWalkthrough-message">
            The fastest way to share someone else’s Tweet with your followers is with a Retweet. Tap the icon to send it instantly.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--reply">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--reply UIWalkthrough-icon">
            </span>
            Join the conversation
           </h3>
           <p class="UIWalkthrough-message">
            Add your thoughts about any Tweet with a Reply. Find a topic you’re passionate about, and jump right in.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--trends">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--discover UIWalkthrough-icon">
            </span>
            Learn the latest
           </h3>
           <p class="UIWalkthrough-message">
            Get instant insight into what people are talking about now.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--wtf">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--follow UIWalkthrough-icon">
            </span>
            Get more of what you love
           </h3>
           <p class="UIWalkthrough-message">
            Follow more accounts to get instant updates about topics you care about.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--search">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--search UIWalkthrough-icon">
            </span>
            Find what's happening
           </h3>
           <p class="UIWalkthrough-message">
            See the latest conversations about any topic instantly.
           </p>
          </div>
          <div class="UIWalkthrough-step UIWalkthrough-step--moments">
           <h3 class="UIWalkthrough-title">
            <span class="Icon Icon--lightning UIWalkthrough-icon">
            </span>
            Never miss a Moment
           </h3>
           <p class="UIWalkthrough-message">
            Catch up instantly on the best stories happening as they unfold.
           </p>
          </div>
         </div>
         <div class="modal-footer">
          <button class="EdgeButton EdgeButton--tertiary u-floatLeft plain-btn UIWalkthrough-button js-previous-step">
           Back
          </button>
          <button class="EdgeButton EdgeButton--secondary UIWalkthrough-button js-next-step js-initial-focus">
           Next
          </button>
         </div>
        </div>
       </div>
      </div>
      <div class="modal-container" id="create-custom-timeline-dialog">
      </div>
      <div class="modal-container" id="edit-custom-timeline-dialog">
      </div>
      <div class="modal-container" id="curate-dialog">
      </div>
      <div class="modal-container" id="media-edit-dialog">
      </div>
      <div class="PermalinkOverlay PermalinkOverlay-with-background " id="permalink-overlay">
       <div class="PermalinkProfile-dismiss modal-close-fixed">
        <span class="Icon Icon--close">
        </span>
       </div>
       <button class="PermalinkOverlay-next PermalinkOverlay-button u-posFixed js-next" type="button">
        <span class="Icon Icon--caretLeft Icon--large">
        </span>
        <span class="u-hiddenVisually">
         Next Tweet from user
        </span>
       </button>
       <div class="PermalinkOverlay-modal">
        <div class="PermalinkOverlay-spinnerContainer u-hidden">
         <div class="PermalinkOverlay-spinner">
         </div>
        </div>
        <div class="PermalinkOverlay-content">
         <div class="PermalinkOverlay-body">
         </div>
        </div>
       </div>
      </div>
      <div class="hidden" id="hidden-content">
       <iframe aria-hidden="true" class="tweet-post-iframe" name="tweet-post-iframe">
       </iframe>
       <iframe aria-hidden="true" class="dm-post-iframe" name="dm-post-iframe">
       </iframe>
      </div>
      <input class="json-data" id="init-data" type="hidden" value='{"keyboardShortcuts":[{"name":"Actions","description":"Shortcuts for common actions.","shortcuts":[{"keys":["Enter"],"description":"Open Tweet details"},{"keys":["o"],"description":"Expand photo"},{"keys":["\/"],"description":"Search"}]},{"name":"Navigation","description":"Shortcuts for navigating between items in timelines.","shortcuts":[{"keys":["?"],"description":"This menu"},{"keys":["j"],"description":"Next Tweet"},{"keys":["k"],"description":"Previous Tweet"},{"keys":["Space"],"description":"Page down"},{"keys":["."],"description":"Load new Tweets"}]},{"name":"Timelines","description":"Shortcuts for navigating to different timelines or pages.","shortcuts":[{"keys":["g","u"],"description":"Go to user\u2026"}]}],"baseFoucClass":"swift-loading","bodyFoucClassNames":"swift-loading no-nav-banners","assetsBasePath":"https:\/\/abs.twimg.com\/a\/1531883619\/","assetVersionKey":"810e1c","emojiAssetsPath":"https:\/\/abs.twimg.com\/emoji\/v2\/72x72\/","environment":"production","formAuthenticityToken":"a1ca0d3455f25d81a0cd641472264bf8915226e3","loggedIn":false,"screenName":null,"fullName":null,"userId":null,"guestId":"153235887260536630","createdAt":null,"needsPhoneVerification":false,"allowAdsPersonalization":true,"scribeBufferSize":3,"pageName":"profile","sectionName":"profile","scribeParameters":{},"recaptchaApiUrl":"https:\/\/www.google.com\/recaptcha\/api\/js\/recaptcha_ajax.js","internalReferer":null,"geoEnabled":false,"typeaheadData":{"accounts":{"enabled":true,"localQueriesEnabled":false,"remoteQueriesEnabled":true,"limit":6},"trendLocations":{"enabled":true},"dmConversations":{"enabled":false},"followedSearches":{"enabled":false},"savedSearches":{"enabled":false,"items":[]},"dmAccounts":{"enabled":false,"localQueriesEnabled":false,"remoteQueriesEnabled":false,"onlyDMable":true},"mediaTagAccounts":{"enabled":false,"localQueriesEnabled":false,"remoteQueriesEnabled":false,"onlyShowUsersWithCanMediaTag":false,"currentUserId":-1},"selectedUsers":{"enabled":false},"prefillUsers":{"enabled":false},"topics":{"enabled":true,"localQueriesEnabled":false,"remoteQueriesEnabled":true,"prefetchLimit":500,"limit":4},"concierge":{"enabled":false,"localQueriesEnabled":false,"remoteQueriesEnabled":false,"prefetchLimit":500,"limit":6},"recentSearches":{"enabled":false},"hashtags":{"enabled":false,"localQueriesEnabled":false,"remoteQueriesEnabled":true,"prefetchLimit":500},"useIndexedDB":false,"showSearchAccountSocialContext":false,"showDebugInfo":false,"useThrottle":true,"accountsOnTop":false,"remoteDebounceInterval":300,"remoteThrottleInterval":300,"tweetContextEnabled":false,"fullNameMatchingInCompose":true,"topicsWithFiltersEnabled":false},"shellReferrer":null,"dm":{"notifications":false,"usePushForNotifications":false,"participant_max":50,"welcome_message_add_to_conversation_enabled":true,"poll_options":{"foreground_poll_interval":3000,"burst_poll_interval":3000,"burst_poll_duration":300000,"max_poll_interval":60000},"card_prefetch":true,"card_prefetch_interval_in_seconds":2000,"dm_quick_reply_options_panel_dismiss_in_ms":2000,"open_dm_enabled":false},"autoplayDisabled":false,"pushStatePageLimit":500000,"routes":{"profile":"\/"},"pushState":true,"viewContainer":"#page-container","href":"\/marswxreport?lang=en","searchPathWithQuery":"\/search?q=query&amp;src=typd","composeAltText":false,"night_mode_activated":false,"user_color":null,"deciders":{"gdprAgeGateDialog":true,"gdprSoftBounceDialog":true,"geo_picker_incident_reset":true,"custom_timeline_curation":false,"native_notifications":true,"disable_ajax_datatype_default_to_text":false,"dm_polling_frequency_in_seconds":3000,"dm_granular_mute_controls":true,"enable_media_tag_prefetch":true,"enableMacawNymizerConversionLanding":false,"hqImageUploads":false,"live_pipeline_consume":true,"mqImageUploads":false,"partnerIdSyncEnabled":true,"sruMediaCategory":true,"photoSruGifLimitMb":15,"promoted_logging_force_post":true,"promoted_video_logging_enabled":true,"pushState":true,"emojiNewCategory":false,"contentEditablePlainTextOnly":false,"web_client_api_stats":false,"web_perftown_stats":true,"web_perftown_ttft":false,"web_client_events_ttft":false,"log_push_state_ttft_metrics":false,"web_sru_stats":false,"web_upload_video":true,"web_upload_video_advanced":false,"upload_video_size":500,"useVmapVariants":false,"autoplayPreviewPreroll":true,"moments_home_module":false,"moments_lohp_enabled":true,"enableNativePush":false,"autoSubscribeNativePush":false,"allowWebPushVapidUpgrade":true,"stickersInteractivity":true,"stickersInteractivityDuringLoading":true,"stickersExperience":true,"dynamic_video_ads_include_long_videos":true,"push_state_size":1000,"live_video_media_control_enabled":false,"cards2_enable_periscope_card_transition":true,"use_api_for_retweet_and_unretweet":false,"use_api_for_follow_and_unfollow":true,"edge_probe_enabled":false,"like_over_http_client":true,"enable_inline_location":true,"enable_tweetstorm_creation":true,"enable_tweetstorm_drafts":false,"enable_tweetstorm_tooltip":true,"text_length_for_tweetstorm_tooltip":50,"dm_report_webview_macaw_swift_enabled":true,"page_title_unread_notification_count":false,"page_title_badge_after_unread_tweets":20},"experiments":{},"toasts_dm":false,"toasts_timeline":false,"toasts_dm_poll_scale":60,"defaultNotificationIcon":"https:\/\/abs.twimg.com\/a\/1531883619\/img\/t1\/mobile\/wp7_app_icon.png","promptbirdData":{"promptbirdEnabled":false,"immediateTriggers":["PullToRefresh","Navigate"],"format":"ProfileOther"},"pageContext":"profile","passwordResetAdvancedLoginForm":true,"skipAutoSignupDialog":false,"shouldReplaceSignupWithLogin":false,"hashflagBaseUrl":"https:\/\/abs.twimg.com\/hashflags\/","activeHashflags":{"growtogether":"GrowTogether_v4\/GrowTogether_v4.png","loveisland":"LoveIsland2018_Flight1\/LoveIsland2018_Flight1.png","payecommezlatan":"Visa_WorldCup2018_v2\/Visa_WorldCup2018_v2.png","beashinboner":"BeAShinboner\/BeAShinboner.png","مسابقة_العربية_للعود":"ArabianOud2018\/ArabianOud2018.png","catarinarainha":"CatarinaEmoji_2018\/CatarinaEmoji_2018.png","jurassicworldfallenkingdom":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","michaelmyersmondays":"HalloweenMovie_2018\/HalloweenMovie_2018.png","織姫":"StarFestivalDay_2018\/StarFestivalDay_2018.png","drnira":"ShowtimeQ3Program_2018\/ShowtimeQ3Program_2018.png","nuestracopa":"Cruzcampo_2018\/Cruzcampo_2018.png","cmtmusicawards":"CMTAwards2018_v2\/CMTAwards2018_v2.png","mymammamia":"MammaMia2_v3\/MammaMia2_v3.png","magicinsandiego":"fantasticbeasts_v4\/fantasticbeasts_v4.png","megatubarão":"TheMeg_2018\/TheMeg_2018.png","nycfireworks":"Macys_Fireworks_2018\/Macys_Fireworks_2018.png","roséwine":"NationalRoseDay2018\/NationalRoseDay2018.png","samsungaddwash":"SpainSamsungAddwash\/SpainSamsungAddwash.png","blindal":"Deadpool2_BlindAl\/Deadpool2_BlindAl.png","thewasp":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","バチェラージャパン":"BachelorJapanS2_v2\/BachelorJapanS2_v2.png","freesmurf":"TNTAnimalKingdomS3\/TNTAnimalKingdomS3.png","abrazodegoles":"ClaroPeru2018_v2\/ClaroPeru2018_v2.png","exoplanet":"2018_0708_0930_weareoneEXO\/2018_0708_0930_weareoneEXO.png","cmgngmtoddy":"ToddyBrasil_2018\/ToddyBrasil_2018.png","informeddelivery":"USPSInformedDelivery\/USPSInformedDelivery.png","teamjurassic":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","انت_بطل":"BeYourOwnChampion_WorldCup\/BeYourOwnChampion_WorldCup.png","gengibraotwist":"PepsiTwist_2018\/PepsiTwist_2018.png","츄바카":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","micheladaclamato":"Clamato_2018\/Clamato_2018.png","porcinet":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","okuldışarıdagünü":"DirtIsGood_Persil\/DirtIsGood_Persil.png","ballparkburger":"BallparkHotDog2018\/BallparkHotDog2018.png","エアアジア":"AirAsia2018_v2\/AirAsia2018_v2.png","ballparkhotdog":"BallparkHotDog2018\/BallparkHotDog2018.png","timesup":"TimesUp_v2\/TimesUp_v2.png","thealienist":"TNT-Alienist\/TNT-Alienist.png","labarramaspower":"Entel_Mundial_Peru_v2\/Entel_Mundial_Peru_v2.png","ハンソロ":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","nacaradogol":"UberWorldCup_2018\/UberWorldCup_2018.png","日野社長":"YokaiWatchWorld_Komasan_v2\/YokaiWatchWorld_Komasan_v2.png","монстрглубины":"TheMeg_2018\/TheMeg_2018.png","totalbedlam":"Deadpool2_Bedlam\/Deadpool2_Bedlam.png","イーヨー":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","juegueargentina":"Naranja_Argentina_WorldCup\/Naranja_Argentina_WorldCup.png","dirtywater":"redsox2018_v2\/redsox2018_v2.png","suncoastproud":"SuperNetball_SunCoastProud\/SuperNetball_SunCoastProud.png","flickertourlive":"NiallHoran2018\/NiallHoran2018.png","بصمة":"ArabianOud2018\/ArabianOud2018.png","animalkingdomtnt":"TNTAnimalKingdomS3\/TNTAnimalKingdomS3.png","hereditary":"A24_Hereditary2018\/A24_Hereditary2018.png","shineonwithreese":"HelloSunshine_2018\/HelloSunshine_2018.png","mntwins":"MinnesotaTwins2018\/MinnesotaTwins2018.png","yanohayexcusas":"SpainSamsungAddwash\/SpainSamsungAddwash.png","itaipavapremium":"ItaipavaMasterchefAmadores\/ItaipavaMasterchefAmadores.png","نصيحة_ناس":"Flynas2018_v2\/Flynas2018_v2.png","exo":"2018_0708_0930_weareoneEXO\/2018_0708_0930_weareoneEXO.png","jackryan":"Amazon_JackRyan_Flight2\/Amazon_JackRyan_Flight2.png","owlmvp":"TMobile_OWLMVP_Flight2_v2\/TMobile_OWLMVP_Flight2_v2.png","pgi":"PubG_eSports_2018\/PubG_eSports_2018.png","dancetothisvideo":"TroyeSivan_ArianaGrande_2018\/TroyeSivan_ArianaGrande_2018.png","プーさん":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","superflymovie":"SuperflyMovie2018\/SuperflyMovie2018.png","ió":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","maisémais":"BrazilNaturaAquarela\/BrazilNaturaAquarela.png","dopinder":"Deadpool2_Dopinder\/Deadpool2_Dopinder.png","thenunpt":"TheNunMovie_2018\/TheNunMovie_2018.png","moveforward":"MoveForward_UberIndia_v2\/MoveForward_UberIndia_v2.png","volvióel3x10":"CristalPeruMundial\/CristalPeruMundial.png","myersmonday":"HalloweenMovie_2018\/HalloweenMovie_2018.png","frose":"NationalRoseDay2018\/NationalRoseDay2018.png","hinchasincondicionales":"MundialMovistar2018_v2\/MundialMovistar2018_v2.png","pgiberlin":"PubG_eSports_2018\/PubG_eSports_2018.png","drunkhistory":"DrunkHistory_2018\/DrunkHistory_2018.png","wnba":"WNBALeagueEmoji\/WNBALeagueEmoji.png","notepierdasnada":"Visa_LatinAmerica_WorldCup\/Visa_LatinAmerica_WorldCup.png","juegaméxico":"coronafutbol2018\/coronafutbol2018.png","themeg":"TheMeg_2018\/TheMeg_2018.png","halloweenmovie":"HalloweenMovie_2018\/HalloweenMovie_2018.png","periscope":"Periscope\/Periscope.png","jurassiclondon":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","catarinavilã":"CatarinaEmoji_2018\/CatarinaEmoji_2018.png","naopercanada":"Visa_LatinAmerica_WorldCup_naopercanada\/Visa_LatinAmerica_WorldCup_naopercanada.png","wantafanta":"FantaSummer2018_WantaFanta\/FantaSummer2018_WantaFanta.png","makeitextra":"Lawrys_MakeItExtra_2018\/Lawrys_MakeItExtra_2018.png","marchforourlivesspotlight":"MarchforOurLivesSpotlight\/MarchforOurLivesSpotlight.png","macysfireworks":"Macys_Fireworks_2018\/Macys_Fireworks_2018.png","roséallday":"NationalRoseDay2018\/NationalRoseDay2018.png","chewbacca":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","ifeelprettyfilm":"feelpretty_v2\/feelpretty_v2.png","experimentojun":"SpainSamsungAddwash\/SpainSamsungAddwash.png","bestoftweets":"BestofTweets2018\/BestofTweets2018.png","amazon":"AmazonPrimeDay_2018\/AmazonPrimeDay_2018.png","whatisfly":"SuperflyMovie2018\/SuperflyMovie2018.png","nialllive":"NiallHoran2018\/NiallHoran2018.png","superflylook":"SuperflyMovie2018\/SuperflyMovie2018.png","animalifantastici":"fantasticbeasts_v3\/fantasticbeasts_v3.png","animauxfantastiques":"fantasticbeasts_v3\/fantasticbeasts_v3.png","theantman":"Disney_AntManMovie_2018\/Disney_AntManMovie_2018.png","rolltide":"Alabama_CFBPlayoff_Teamv3\/Alabama_CFBPlayoff_Teamv3.png","بطل_جنب_بطلة":"HeroNextToHero_v3\/HeroNextToHero_v3.png","lovetwitter":"LoveTwitter\/LoveTwitter.png","もしもマンガが全巻無料なら":"NTTSolmare2018_v2\/NTTSolmare2018_v2.png","endalz":"AlzheimersAssociation2018_v2\/AlzheimersAssociation2018_v2.png","тигруля":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","rootedinoakland":"OaklandAthletics2018\/OaklandAthletics2018.png","texasrangers":"TexasRangers2018\/TexasRangers2018.png","yoconstruyopais":"Bancolombia_Flight2\/Bancolombia_Flight2.png","macys4thofjulyfireworks":"Macys_Fireworks_2018\/Macys_Fireworks_2018.png","anittamedicina":"Anitta_SurpriseSingle\/Anitta_SurpriseSingle.png","tebancamosselección":"Naranja_Argentina_WorldCup\/Naranja_Argentina_WorldCup.png","mammamia":"MammaMia2_v3\/MammaMia2_v3.png","dttpremiere":"TroyeSivan_ArianaGrande_2018\/TroyeSivan_ArianaGrande_2018.png","ungolunpotrero":"Naranja_Argentina_WorldCup\/Naranja_Argentina_WorldCup.png","biaarantes":"BriceEmoji_2018\/BriceEmoji_2018.png","آية_وقيمة":"MiskValues2018\/MiskValues2018.png","espejopublico":"EspejoPublico_2017_2018\/EspejoPublico_2017_2018.png","badisbred":"TNTAnimalKingdomS3\/TNTAnimalKingdomS3.png","télépéage":"Ulys_2018\/Ulys_2018.png","votebwp":"MLS_AllStarCaptains_BWP\/MLS_AllStarCaptains_BWP.png","lajugadaganadora":"MundialClaro_2018\/MundialClaro_2018.png","rwc7s":"Rugby7s_WorldCup_2018\/Rugby7s_WorldCup_2018.png","chewie":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","flywithadditive":"GEAdaptive_2018_FlyWithAdditive\/GEAdaptive_2018_FlyWithAdditive.png","soloastarwarsstory":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","symbiote":"Venom_2018\/Venom_2018.png","rockies25th":"ColoradoRockies2018\/ColoradoRockies2018.png","よまにゃ":"ShueishaBrand_2018_v4\/ShueishaBrand_2018_v4.png","медвежоноквинни":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","bethechange":"BeTheChange_v2\/BeTheChange_v2.png","лэндо":"StarWarsSolo_Lando\/StarWarsSolo_Lando.png","followtheball":"waltdisneyoscars2018\/waltdisneyoscars2018.png","valla":"FranceBlizzardOWL_LAValiant\/FranceBlizzardOWL_LAValiant.png","comigoninguémtoddy":"ToddyBrasil_ComigoNinguemToddy\/ToddyBrasil_ComigoNinguemToddy.png","tigro":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","escutemedicina":"Anitta_SurpriseSingle\/Anitta_SurpriseSingle.png","crimesofgrindelwald":"fantasticbeasts_v4\/fantasticbeasts_v4.png","statebankofindia":"SBIBank_2018_Flight2\/SBIBank_2018_Flight2.png","erranmorad":"ShowtimeQ3Program_2018\/ShowtimeQ3Program_2018.png","shieldsup":"FranceBlizzardOWL_LAGladiators\/FranceBlizzardOWL_LAGladiators.png","thechevroletrace":"TheChevroletRace_2018\/TheChevroletRace_2018.png","boomsday":"FranceBlizzard_Hearthstone_2018\/FranceBlizzard_Hearthstone_2018.png","millenniumfalcon":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","صقورنا_قدها":"SaudiAirline_2018\/SaudiAirline_2018.png","loveislandaftersun":"LoveIsland2018_Flight1\/LoveIsland2018_Flight1.png","wannasprite":"Sprite_summer2018\/Sprite_summer2018.png","eatatpanorama":"PanoramaFestival_2018\/PanoramaFestival_2018.png","unmomentoespecial":"ABIMexico_ModeloCafe\/ABIMexico_ModeloCafe.png","ダブルウェア":"EsteeLauder_DoubleWear\/EsteeLauder_DoubleWear.png","somosnuevaraza":"Bancolombia_SomosNuevaRaza\/Bancolombia_SomosNuevaRaza.png","mercwithamouth":"Deadpool2_Deadpool\/Deadpool2_Deadpool.png","labarramáspower":"Entel_Mundial_Peru_v2\/Entel_Mundial_Peru_v2.png","7afl":"AFL2018\/AFL2018.png","michelada":"Clamato_2018\/Clamato_2018.png","amtodmbfn":"BuzzFeedMorning_v3\/BuzzFeedMorning_v3.png","bachelorjapan":"BachelorJapanS2_v2\/BachelorJapanS2_v2.png","torcidan1":"brahma_flight2\/brahma_flight2.png","asksweetbitter":"STARZSweetbitter18\/STARZSweetbitter18.png","ナツイチの日":"ShueishaBrand_2018_v4\/ShueishaBrand_2018_v4.png","venommovie":"Venom_2018\/Venom_2018.png","mammamia2movie":"MammaMia2_v3\/MammaMia2_v3.png","amália":"AmaliaEmoji_2018\/AmaliaEmoji_2018.png","juntosmiami":"MiamiMarlins2018\/MiamiMarlins2018.png","myxmusicawards2018":"MYXMusicAwards2018\/MYXMusicAwards2018.png","toystoryland":"waltdisneyoscars2018\/waltdisneyoscars2018.png","onthebus":"NRLTigers2018\/NRLTigers2018.png","allontheline":"SuperNetball_Allontheline\/SuperNetball_Allontheline.png","btsxspotify":"SpotifyBTS2018_v2\/SpotifyBTS2018_v2.png","fallenkingdom":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","마이베스트일레븐":"MyBestEleven2018\/MyBestEleven2018.png","jurassicnight":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","ulys":"Ulys_2018\/Ulys_2018.png","アントマン":"Disney_Antman_2018\/Disney_Antman_2018.png","letsgobucs":"PittsburghPirates2018\/PittsburghPirates2018.png","١٠٠_متعة_في_القيادة":"VW_JoysofDriving\/VW_JoysofDriving.png","مسابقة_طيران_ناس":"Flynas2018_v2\/Flynas2018_v2.png","جمعية_زمزم_لجسد_واحد":"ZamzamSociety2018\/ZamzamSociety2018.png","comicstaan":"APVIndiaComicstaan_v2\/APVIndiaComicstaan_v2.png","nestleextreme":"NestleExtreme_2018\/NestleExtreme_2018.png","rosé":"NationalRoseDay2018\/NationalRoseDay2018.png","waspwings":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","ワスプ":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","lovevshate":"BlackKlansmanMovie\/BlackKlansmanMovie.png","mammamiaherewegoagain":"MammaMia2_v3\/MammaMia2_v3.png","оса":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","smallfoot":"WM_Smallfoot\/WM_Smallfoot.png","alentadoresseriales":"YPHArgentina_WorldCup\/YPHArgentina_WorldCup.png","amtodm":"BuzzFeedMorning_v3\/BuzzFeedMorning_v3.png","maythefourth":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","qira":"StarWarsSolo_Qira\/StarWarsSolo_Qira.png","got7":"GOT7WORLDTOUR_2018\/GOT7WORLDTOUR_2018.png","sharpobjectshbo":"HBOSharpObjects\/HBOSharpObjects.png","thematriline":"A24_Hereditary2018\/A24_Hereditary2018.png","iamopl":"iamopl_v2\/iamopl_v2.png","shocktheworld":"FranceBlizzardOWL_SanFrancisco\/FranceBlizzardOWL_SanFrancisco.png","amyadams":"HBOSharpObjects\/HBOSharpObjects.png","นักบอลแซ่บ":"KbankxWorldcup\/KbankxWorldcup.png","am2dmbf":"BuzzFeedMorning_v3\/BuzzFeedMorning_v3.png","もんげー":"YokaiWatchWorld_Komasan_v2\/YokaiWatchWorld_Komasan_v2.png","妖怪ウォッチ":"YokaiWatchWorld_Jibanyan\/YokaiWatchWorld_Jibanyan.png","amáliaguerreira":"AmaliaEmoji_2018\/AmaliaEmoji_2018.png","eddiesclubhouse":"Venom_2018\/Venom_2018.png","itseeyore":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","hansolo":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","tictocnews":"bloombergtictoc2018\/bloombergtictoc2018.png","thefourfox":"Fox_TheFour_Season2\/Fox_TheFour_Season2.png","winniepuuh":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","ガチ勢応援":"GatsbyDeo2018\/GatsbyDeo2018.png","hereditarymovie":"A24_Hereditary2018\/A24_Hereditary2018.png","alômãe":"BrazilWorldCup2018_AloMae_v3\/BrazilWorldCup2018_AloMae_v3.png","sorrytobotheryou":"SorryToBotherYou2018\/SorryToBotherYou2018.png","جرير_توصل":"Jarir2018\/Jarir2018.png","jurassic":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","addwash":"SpainSamsungAddwash\/SpainSamsungAddwash.png","walk2endalz":"AlzheimersAssociation2018_v2\/AlzheimersAssociation2018_v2.png","endalzheimers":"AlzheimersAssociation2018_v2\/AlzheimersAssociation2018_v2.png","nationaldinoday":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","zeitgeist116":"Deadpool2_Zeitgeist\/Deadpool2_Zeitgeist.png","thefuturelooksfunny":"APVIndiaComicstaan_v2\/APVIndiaComicstaan_v2.png","exo_comingsoon":"2018_0708_0930_weareoneEXO\/2018_0708_0930_weareoneEXO.png","kohlscash":"KohlsCash_Q3_2018\/KohlsCash_Q3_2018.png","sheshines":"HelloSunshine_2018\/HelloSunshine_2018.png","blackkklansmanmovie":"BlackKlansmanMovie\/BlackKlansmanMovie.png","fantasticbeasts":"fantasticbeasts_v3\/fantasticbeasts_v3.png","コマさん":"YokaiWatchWorld_Komasan_v2\/YokaiWatchWorld_Komasan_v2.png","scratchoftheday":"WilliamHillWorldCup2018_v2\/WilliamHillWorldCup2018_v2.png","bluejays":"TorontoBlueJays2018_v3\/TorontoBlueJays2018_v3.png","thatssuperfly":"SuperflyMovie2018\/SuperflyMovie2018.png","adoptadino":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","winniethepooh":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","mammamiafilm":"MammaMia2_v3\/MammaMia2_v3.png","printmeaflight":"GEAdaptive_2018_v3\/GEAdaptive_2018_v3.png","prixbestoftweets":"BestofTweets2018\/BestofTweets2018.png","ballparkgrillin":"BallparkHotDog2018\/BallparkHotDog2018.png","بطاقة_كفاءة_الطاقة":"SaudiEnergyEfficiencyCenter\/SaudiEnergyEfficiencyCenter.png","maythefourthbewithyou":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","landocalrissian":"StarWarsSolo_Lando\/StarWarsSolo_Lando.png","amáliarainha":"AmaliaEmoji_2018\/AmaliaEmoji_2018.png","redv":"NRLRedV2018\/NRLRedV2018.png","앤트맨":"Disney_Antman_2018\/Disney_Antman_2018.png","sweetbittertv":"STARZSweetbitter18\/STARZSweetbitter18.png","rallytogether":"Cleveland2018\/Cleveland2018.png","mentellall":"TheBachelorette2018\/TheBachelorette2018.png","tca":"TeenChoiceAwards_2018\/TeenChoiceAwards_2018.png","westworld":"HBOWestworld_Finale\/HBOWestworld_Finale.png","starwarsday":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","pagacomozlatan":"Visa_WorldCup2018_v2\/Visa_WorldCup2018_v2.png","bostonup":"FranceBlizzardOWL_Boston\/FranceBlizzardOWL_Boston.png","everybodyin":"ChicagoCubs2018\/ChicagoCubs2018.png","antmanmovie":"Disney_AntManMovie_2018\/Disney_AntManMovie_2018.png","bestoftweetsawards":"BestofTweets2018\/BestofTweets2018.png","avancamos":"BrazillianFederalGov_Avancamos\/BrazillianFederalGov_Avancamos.png","jordanpeele":"BlackKlansmanMovie\/BlackKlansmanMovie.png","プリコネ":"PriconneRedive2018\/PriconneRedive2018.png","spikelee":"BlackKlansmanMovie\/BlackKlansmanMovie.png","gotitfrommymom":"A24_Hereditary2018\/A24_Hereditary2018.png","blackkklansmanfilm":"BlackKlansmanMovie\/BlackKlansmanMovie.png","tonicollette":"A24_Hereditary2018\/A24_Hereditary2018.png","flynas":"Flynas2018_v2\/Flynas2018_v2.png","jurassicpark":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","100joysofdriving":"VW_JoysofDriving\/VW_JoysofDriving.png","powertv":"STARZPower_S5_Ghost\/STARZPower_S5_Ghost.png","إثراء_رمضان":"ArabLeadersSummit2018_v4\/ArabLeadersSummit2018_v4.png","dominomf":"Deadpool2_Domino\/Deadpool2_Domino.png","이요르":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","위니더푸":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","เดอะนัน":"TheNunMovie_2018\/TheNunMovie_2018.png","frosé":"NationalRoseDay2018\/NationalRoseDay2018.png","キリンレモントリビュート":"KirinLemon90thAnniversary_2018\/KirinLemon90thAnniversary_2018.png","dodgers":"LADodgers2018\/LADodgers2018.png","avançamos":"BrazillianFederalGov_Avancamos\/BrazillianFederalGov_Avancamos.png","dancetothis":"TroyeSivan_ArianaGrande_2018\/TroyeSivan_ArianaGrande_2018.png","loveislandpodcast":"LoveIsland2018_Flight2\/LoveIsland2018_Flight2.png","cable":"Deadpool2_Cable\/Deadpool2_Cable.png","قدام_معنا":"FordSaudiWomenDrive\/FordSaudiWomenDrive.png","partyroyale":"ForniteBattleRoyale2018\/ForniteBattleRoyale2018.png","onepursuit":"WashingtonNationals2018\/WashingtonNationals2018.png","tudopelaselecao":"GuaranaCopa_2018\/GuaranaCopa_2018.png","wearegeelong":"WeAreGeelong_v2\/WeAreGeelong_v2.png","proudibmer":"IBMThink2018_extension\/IBMThink2018_extension.png","blackklansman":"BlackKlansmanMovie\/BlackKlansmanMovie.png","nationaldinosaurday":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","ih-oh":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","sbinews":"SBIBank_2018_Flight2\/SBIBank_2018_Flight2.png","deadpool2":"Deadpool2_Deadpool\/Deadpool2_Deadpool.png","happymammasday":"MammaMia2_v3\/MammaMia2_v3.png","mammamiamovie":"MammaMia2_v3\/MammaMia2_v3.png","ڤيمتو":"Vimto2018\/Vimto2018.png","gorabbitohs":"NRLsouths2018\/NRLsouths2018.png","roadtochange":"MarchforOurLives_RoadToChange\/MarchforOurLives_RoadToChange.png","põepraforasuascores":"BrazilNaturaAquarela\/BrazilNaturaAquarela.png","wannafanta":"FantaSummer2018\/FantaSummer2018.png","tanabata":"StarFestivalDay_2018\/StarFestivalDay_2018.png","чубакка":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","dubnation":"NBA_2018_19_GSW_extension\/NBA_2018_19_GSW_extension.png","beautyinai":"HuaweiHonorQ2GlobalLaunch_v2\/HuaweiHonorQ2GlobalLaunch_v2.png","carriebradshaw":"HBOSexandtheCity2018\/HBOSexandtheCity2018.png","teamghost":"STARZPower_S5_Ghost\/STARZPower_S5_Ghost.png","starwars":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","eddiebrock":"Venom_2018\/Venom_2018.png","dejemostodo":"Naranja_Argentina_WorldCup\/Naranja_Argentina_WorldCup.png","bienvoyager":"Ulys_2018\/Ulys_2018.png","generationdbacks":"ArizonaDBacks_v2\/ArizonaDBacks_v2.png","thefour":"Fox_TheFour_Season2\/Fox_TheFour_Season2.png","niallhoranlive":"NiallHoran2018\/NiallHoran2018.png","summergrilling":"BallparkHotDog2018\/BallparkHotDog2018.png","sweetbitterstarz":"STARZSweetbitter18\/STARZSweetbitter18.png","airasia":"AirAsia2018_v2\/AirAsia2018_v2.png","ifeelprettymovie":"feelpretty_v2\/feelpretty_v2.png","七夕":"StarFestivalDay_2018\/StarFestivalDay_2018.png","アントマンとワスプ":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","マイベストイレブン":"MyBestEleven2018\/MyBestEleven2018.png","globalcitizen":"GlobalCitizenFestival_2018\/GlobalCitizenFestival_2018.png","проклятиемонахини":"TheNunMovie_2018\/TheNunMovie_2018.png","кира":"StarWarsSolo_Qira\/StarWarsSolo_Qira.png","juntossomos10":"MastercardSoccer\/MastercardSoccer.png","megatubarao":"TheMeg_2018\/TheMeg_2018.png","juegamexico":"coronafutbol2018\/coronafutbol2018.png","negasonicteenagewarhead":"Deadpool2_Negasonic\/Deadpool2_Negasonic.png","afl":"AFL18\/AFL18.png","チューバッカ":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","نقدر_نفرحهم":"ZamzamSociety2018\/ZamzamSociety2018.png","bienarriver":"Ulys_2018\/Ulys_2018.png","pdomjnate":"FranceBlizzardOWL_Philadelphia\/FranceBlizzardOWL_Philadelphia.png","크리스토퍼로빈과곰돌이푸":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","messiwithooredoo":"Ooredoo_WorldCup\/Ooredoo_WorldCup.png","teamkanan":"STARZPower_S5_Kanan\/STARZPower_S5_Kanan.png","espiglet":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","pimpi":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","todasascoresdasuabeleza":"BrazilNaturaAquarela\/BrazilNaturaAquarela.png","thedynastybegins":"FranceBlizzardOWL_Seoul\/FranceBlizzardOWL_Seoul.png","windgap":"HBOSharpObjects\/HBOSharpObjects.png","owl2018":"OverwatchLeague_WorldFinals_2018\/OverwatchLeague_WorldFinals_2018.png","ifeelpretty":"feelpretty_v2\/feelpretty_v2.png","rusiaentusmanosconclaro":"MundialClaro_2018\/MundialClaro_2018.png","miskvalues":"MiskValues2018\/MiskValues2018.png","ジバニャン":"YokaiWatchWorld_Jibanyan\/YokaiWatchWorld_Jibanyan.png","nowruz":"nowruz2018_v4\/nowruz2018_v4.png","rosewine":"NationalRoseDay2018\/NationalRoseDay2018.png","dinosaurday":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","yetivillage":"WM_Smallfoot\/WM_Smallfoot.png","デレステ":"ImagscgStage2018\/ImagscgStage2018.png","tigrou":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","thisismycrew":"MilwaukeeBrewers2018\/MilwaukeeBrewers2018.png","cmtawards2018":"CMTAwards2018_v2\/CMTAwards2018_v2.png","shatterstar":"Deadpool2_Shatterstar\/Deadpool2_Shatterstar.png","firetvcube":"FireTVLaunch2018\/FireTVLaunch2018.png","teampeter":"Deadpool2_PeterW\/Deadpool2_PeterW.png","votevela":"MLS_AllStarCaptains_Vela\/MLS_AllStarCaptains_Vela.png","앤트맨과와스프":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","laavispa":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","alentemosunidos":"CristalPeruMundial\/CristalPeruMundial.png","codyboys":"TNTAnimalKingdomS3\/TNTAnimalKingdomS3.png","antman":"Disney_Antman_2018\/Disney_Antman_2018.png","zahlewiezlatan":"Visa_WorldCup2018_v2\/Visa_WorldCup2018_v2.png","eeyore":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","satc20":"HBOSexandtheCity2018\/HBOSexandtheCity2018.png","energíaargentina":"YPHArgentina_WorldCup\/YPHArgentina_WorldCup.png","theshape":"HalloweenMovie_2018\/HalloweenMovie_2018.png","solostarwars":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","govixens":"SuperNetball_GoVixens\/SuperNetball_GoVixens.png","ariaster":"A24_Hereditary2018\/A24_Hereditary2018.png","mytwitteranniversary":"MyTwitterAnniversary\/MyTwitterAnniversary.png","thrunthru":"NRLtitans2018\/NRLtitans2018.png","statebank":"SBIBank_2018_Flight2\/SBIBank_2018_Flight2.png","สวัสดีบอลโลก":"TrueCorp_WorldCup_2018\/TrueCorp_WorldCup_2018.png","مسك_القيم":"MiskValues2018\/MiskValues2018.png","iaah":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","comicstaantrailer":"APVIndiaComicstaan_v2\/APVIndiaComicstaan_v2.png","cheddarlive":"Cheddar_Emoji_v4\/Cheddar_Emoji_v4.png","ferkel":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","アクアマン":"Aquaman_2018\/Aquaman_2018.png","blackkklansman":"BlackKlansmanMovie\/BlackKlansmanMovie.png","それは最悪の一周年":"Sinoalice2018\/Sinoalice2018.png","teenchoiceawards":"TeenChoiceAwards_2018\/TeenChoiceAwards_2018.png","جمعية_زمزم":"ZamzamSociety2018\/ZamzamSociety2018.png","ティガー":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","peterw":"Deadpool2_PeterW\/Deadpool2_PeterW.png","antmanandthewasp":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","myx21myfifaworldcup":"Vivo_FIFA_2018\/Vivo_FIFA_2018.png","إثراء":"ArabLeadersSummit2018_v4\/ArabLeadersSummit2018_v4.png","tudopronto":"CocaColaFWC_2018\/CocaColaFWC_2018.png","letsmarchnova":"VillanovaYearLong\/VillanovaYearLong.png","alomae":"BrazilWorldCup2018_AloMae_v3\/BrazilWorldCup2018_AloMae_v3.png","haloson":"haloson\/haloson.png","綾鷹ほうじ茶":"cocacolaAyataka3\/cocacolaAyataka3.png","hinchaincondicional":"MundialMovistar2018_v2\/MundialMovistar2018_v2.png","fortheloveofhotdogs":"OscarMayer_Weinermobile\/OscarMayer_Weinermobile.png","tecnomobile":"TranssionTecno2018\/TranssionTecno2018.png","スターウォーズ":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","weareoneexo":"2018_0708_0930_weareoneEXO\/2018_0708_0930_weareoneEXO.png","hansolostarwars":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","tudopelaseleçao":"GuaranaCopa_2018\/GuaranaCopa_2018.png","ランドカルリジアン":"StarWarsSolo_Lando\/StarWarsSolo_Lando.png","clamato":"Clamato_2018\/Clamato_2018.png","spotifyloveyourself":"SpotifyBTS2018_v2\/SpotifyBTS2018_v2.png","motog6":"MotorolaG62018\/MotorolaG62018.png","sexandthecity20":"HBOSexandtheCity2018\/HBOSexandtheCity2018.png","tvoshortdoc":"TVOShortDocs\/TVOShortDocs.png","itspiglet":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","homemformiga":"Disney_Antman_2018\/Disney_Antman_2018.png","weflyasone":"weflyasone_v2\/weflyasone_v2.png","familyoftheyear":"ArrestedDevelopment2018\/ArrestedDevelopment2018.png","flyeaglesfly":"Eaglesv4\/Eaglesv4.png","podictions":"LoveIsland2018_Flight2\/LoveIsland2018_Flight2.png","티거":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","flywithairasia":"AirAsia2018_v2\/AirAsia2018_v2.png","человекмуравей":"Disney_Antman_2018\/Disney_Antman_2018.png","bbklivedesconocido":"NestleExtreme_2018\/NestleExtreme_2018.png","budlighthouseparty":"BudLight_HouseParty_2018\/BudLight_HouseParty_2018.png","alienisttnt":"TNT-Alienist\/TNT-Alienist.png","ウィスパー":"YokaiWatchWorld_Whisper\/YokaiWatchWorld_Whisper.png","westworldhbo":"HBOWestworld_Finale\/HBOWestworld_Finale.png","espooh":"ChristopherRobin_ItsPooh2018\/ChristopherRobin_ItsPooh2018.png","energiaquenosune":"YPHArgentina_WorldCup\/YPHArgentina_WorldCup.png","netneutrality":"Net_Emoji_v3\/Net_Emoji_v3.png","кристоферробин":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","wheresbaz":"TNTAnimalKingdomS3\/TNTAnimalKingdomS3.png","thealienisttnt":"TNT-Alienist\/TNT-Alienist.png","yonobysbi":"SBIBank_2018_Flight2\/SBIBank_2018_Flight2.png","roseallday":"NationalRoseDay2018\/NationalRoseDay2018.png","綾鷹":"cocacolaAyataka3\/cocacolaAyataka3.png","amtodmbf":"BuzzFeedMorning_v3\/BuzzFeedMorning_v3.png","theelyxion_dot":"2018_0708_0930_weareoneEXO\/2018_0708_0930_weareoneEXO.png","اداء_الابطال":"BeYourOwnChampion_WorldCup\/BeYourOwnChampion_WorldCup.png","internetpower":"Entel_Mundial_Peru_v2\/Entel_Mundial_Peru_v2.png","clawstnt":"TNTClawsS2\/TNTClawsS2.png","schinnonordestão":"SchinNordestao2018\/SchinNordestao2018.png","venomsymbiote":"Venom_2018\/Venom_2018.png","レベルファイブ":"YokaiWatchWorld_Jibanyan\/YokaiWatchWorld_Jibanyan.png","プリ米":"PriconneRedive2018\/PriconneRedive2018.png","aviationseason":"GEAdaptive_2018_v3\/GEAdaptive_2018_v3.png","makeamericabluthagain":"ArrestedDevelopment2018\/ArrestedDevelopment2018.png","お茶にしましょう綾鷹":"cocacolaAyataka3\/cocacolaAyataka3.png","fortnite":"ForniteBattleRoyale2018\/ForniteBattleRoyale2018.png","funaayega":"APVIndiaComicstaan_v2\/APVIndiaComicstaan_v2.png","nbatwitter":"NBATwitter_Emoji___v5\/NBATwitter_Emoji___v5.png","bemorehuman":"ReebokWomens_2018\/ReebokWomens_2018.png","flythefuture":"GEAdaptive_2018_v3\/GEAdaptive_2018_v3.png","upupcronulla":"NRLsharks2018\/NRLsharks2018.png","inplaywithray":"bet365RayWinstone_v2\/bet365RayWinstone_v2.png","chelaycafé":"ABIMexico_ModeloCafe\/ABIMexico_ModeloCafe.png","كفاءة":"SaudiEnergyEfficiencyCenter\/SaudiEnergyEfficiencyCenter.png","themegza":"TheMeg_2018\/TheMeg_2018.png","bebold":"PhiladelphiaPhillies2018\/PhiladelphiaPhillies2018.png","infiltratehate":"BlackKlansmanMovie\/BlackKlansmanMovie.png","tvoshortdocs":"TVOShortDocs\/TVOShortDocs.png","poptarts":"PopTarts_2018\/PopTarts_2018.png","flyfridays":"SuperflyMovie2018\/SuperflyMovie2018.png","torcedorfanatico":"RexonaWorldCupEmoji\/RexonaWorldCupEmoji.png","ピグレット":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","vistarapremiumeconomy":"Vistara_2018\/Vistara_2018.png","prixbestoftweet":"BestofTweets2018\/BestofTweets2018.png","wadewilson":"Deadpool2_Deadpool\/Deadpool2_Deadpool.png","outdoorclassroomday":"DirtIsGood_Persil\/DirtIsGood_Persil.png","بطله_جنب_بطل":"HeroNextToHero_v3\/HeroNextToHero_v3.png","primeday":"AmazonPrimeDay_2018\/AmazonPrimeDay_2018.png","diadeaprenderbrincando":"DirtIsGood_Persil\/DirtIsGood_Persil.png","осликушастик":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","集英社文庫":"ShueishaBrand_2018_v4\/ShueishaBrand_2018_v4.png","medicinaanitta":"Anitta_SurpriseSingle\/Anitta_SurpriseSingle.png","مركز_الملك_عبدالعزيز_الثقافي":"ArabLeadersSummit2018_v4\/ArabLeadersSummit2018_v4.png","eneauxtroubles":"TheMeg_2018\/TheMeg_2018.png","giomonaldo":"ShowtimeQ3Program_2018\/ShowtimeQ3Program_2018.png","tigger":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","unbelievablygood":"Vistara_2018\/Vistara_2018.png","johndavidwashington":"BlackKlansmanMovie\/BlackKlansmanMovie.png","begiant":"GWSGIANTS\/GWSGIANTS.png","bourriquet":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","nationalroséday":"NationalRoseDay2018\/NationalRoseDay2018.png","sweetbitter":"STARZSweetbitter18\/STARZSweetbitter18.png","wcclassics":"WilliamHillWorldCup2018_v2\/WilliamHillWorldCup2018_v2.png","melbourneproud":"NRLmelbourne2018\/NRLmelbourne2018.png","ナツイチ":"ShueishaBrand_2018_v4\/ShueishaBrand_2018_v4.png","sweetbitterpremiere":"STARZSweetbitter18\/STARZSweetbitter18.png","freshevents":"FreshEmpire_Q3_v2\/FreshEmpire_Q3_v2.png","lamamámáspower":"Entel_Mundial_Peru_v2\/Entel_Mundial_Peru_v2.png","leitão":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","wakandaweekend":"BlackPantherHomeEnt2018\/BlackPantherHomeEnt2018.png","wearevenom":"Venom_2018\/Venom_2018.png","sfgiants":"SFGiants2018\/SFGiants2018.png","incondicionales":"MundialMovistar2018_v2\/MundialMovistar2018_v2.png","directorx":"SuperflyMovie2018\/SuperflyMovie2018.png","am2dm":"BuzzFeedMorning_v3\/BuzzFeedMorning_v3.png","modelocafé":"ABIMexico_ModeloCafe\/ABIMexico_ModeloCafe.png","whatblackpanthermeanstome":"BlackPantherHomeEnt2018\/BlackPantherHomeEnt2018.png","chelaocafé":"ABIMexico_ModeloCafe\/ABIMexico_ModeloCafe.png","homemformigaeavespa":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","bachelornation":"TheBachelorette2018\/TheBachelorette2018.png","wnbatakesastand":"WNBATakesAStand3\/WNBATakesAStand3.png","venom":"Venom_2018\/Venom_2018.png","tuiteratura":"FeriaDelHilo\/FeriaDelHilo.png","burnblue":"FranceBlizzardOWL_Dallas\/FranceBlizzardOWL_Dallas.png","aisnextgxpeckbambam":"PECKBAMBAM_2018\/PECKBAMBAM_2018.png","gotgrit":"SuperNetball_gotgrit\/SuperNetball_gotgrit.png","lanonne":"TheNunMovie_2018\/TheNunMovie_2018.png","iamfirebird":"SuperNetball_IAMFIREBIRD\/SuperNetball_IAMFIREBIRD.png","mybesteleven":"MyBestEleven2018\/MyBestEleven2018.png","キリンレモンのうた":"KirinLemon90thAnniversary_2018\/KirinLemon90thAnniversary_2018.png","abrazodegol":"ClaroPeru2018_v2\/ClaroPeru2018_v2.png","igór":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","capturehistory":"OverwatchLeague_WorldFinals_2018\/OverwatchLeague_WorldFinals_2018.png","powerstarz":"STARZPower_S5_Ghost\/STARZPower_S5_Ghost.png","usps":"USPSInformedDelivery\/USPSInformedDelivery.png","โคตรหลามพันล้านปี":"TheMeg_2018\/TheMeg_2018.png","energíaquenosune":"YPHArgentina_EnergiaQueNosUne\/YPHArgentina_EnergiaQueNosUne.png","redscountry":"CincinnatiReds2018\/CincinnatiReds2018.png","プリコネ無料10連ガチャ":"PriconneRedive2018\/PriconneRedive2018.png","superflysoundtrack":"SuperflyMovie2018\/SuperflyMovie2018.png","advancingaviation":"GEAdaptive_2018_v3\/GEAdaptive_2018_v3.png","powerpremiere":"STARZPower_S5_Ghost\/STARZPower_S5_Ghost.png","bricedsr":"BriceEmoji_2018\/BriceEmoji_2018.png","loveyourselfxspotify":"SpotifyBTS2018_v2\/SpotifyBTS2018_v2.png","votebluth":"ArrestedDevelopment2018\/ArrestedDevelopment2018.png","amáliaplebeia":"AmaliaEmoji_2018\/AmaliaEmoji_2018.png","teenchoice":"TeenChoiceAwards_2018\/TeenChoiceAwards_2018.png","comessasbolinhasngmtoddy":"ToddyBrasil_2018\/ToddyBrasil_2018.png","satanicgrandma":"A24_Hereditary2018\/A24_Hereditary2018.png","brunamarquezine":"CatarinaEmoji_2018\/CatarinaEmoji_2018.png","cmtawards":"CMTAwards2018_v2\/CMTAwards2018_v2.png","jurassicjune":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","jurassicpark25":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","yoconstruyopaís":"Bancolombia_Flight2\/Bancolombia_Flight2.png","cmtawards18":"CMTAwards2018_v2\/CMTAwards2018_v2.png","comigoninguemtoddy":"ToddyBrasil_2018\/ToddyBrasil_2018.png","แพ้ก็พลัสชนะก็พลัส":"KbankxWorldcup\/KbankxWorldcup.png","avespa":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","푸":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","gotiges":"gotiges\/gotiges.png","thesecondcoming":"Deadpool2_Deadpool\/Deadpool2_Deadpool.png","aquaman":"Aquaman_2018\/Aquaman_2018.png","mamamia2":"MammaMia2_v3\/MammaMia2_v3.png","estigger":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","ridemcowboys":"NRLcowboys2018_v2\/NRLcowboys2018_v2.png","teamforpirlo":"UberEats_WorldCup\/UberEats_WorldCup.png","طيب_الله_فالك":"ArabianOud2018\/ArabianOud2018.png","letsgonewarriors":"LetsGoneWarriors_v2\/LetsGoneWarriors_v2.png","flexweave":"reebokflexweave_v2\/reebokflexweave_v2.png","tudopelaselecão":"GuaranaCopa_2018\/GuaranaCopa_2018.png","thefouronfox":"Fox_TheFour_Season2\/Fox_TheFour_Season2.png","nationalroseday":"NationalRoseDay2018\/NationalRoseDay2018.png","피글렛":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","hwc2018":"HockeyWomensWorldCup_2018\/HockeyWomensWorldCup_2018.png","eatlikeapro":"EatLikeAPro2018V2\/EatLikeAPro2018V2.png","turnupthelove":"ATT_TurnUpTheLove_v2\/ATT_TurnUpTheLove_v2.png","الخطوط_توديك_روسيا":"SaudiAirline_2018\/SaudiAirline_2018.png","schinnonordestao":"SchinNordestao2018\/SchinNordestao2018.png","halloweenmovieofficial":"HalloweenMovie_2018\/HalloweenMovie_2018.png","tebancamosseleccion":"Naranja_Argentina_TeBancamosSeleccion\/Naranja_Argentina_TeBancamosSeleccion.png","한솔로":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","safetyatheart":"MoveForward_UberIndia_v2\/MoveForward_UberIndia_v2.png","shotenroute":"MoveForward_UberIndia_v2\/MoveForward_UberIndia_v2.png","christopherrobin":"ChristopherRobin_ChristopherRobinfix\/ChristopherRobin_ChristopherRobinfix.png","lamamamaspower":"Entel_Mundial_Peru_v2\/Entel_Mundial_Peru_v2.png","comicstaanlive":"APVIndiaComicstaan_v2\/APVIndiaComicstaan_v2.png","키라":"StarWarsSolo_Qira\/StarWarsSolo_Qira.png","winnielourson":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","100億円ガチャ":"Sinoalice2018\/Sinoalice2018.png","luckydomino":"Deadpool2_Domino\/Deadpool2_Domino.png","marchforourlives":"marchforourlives\/marchforourlives.png","لتبقى":"SaudiEnergyEfficiencyCenter\/SaudiEnergyEfficiencyCenter.png","シノアリス一周年":"Sinoalice2018\/Sinoalice2018.png","okuldisaridagunu":"DirtIsGood_Persil\/DirtIsGood_Persil.png","loespeciales":"ABIMexico_ModeloCafe\/ABIMexico_ModeloCafe.png","jurassicworld":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","emaargoldenhome":"EmaarGoldenHome\/EmaarGoldenHome.png","thebachelorette":"TheBachelorette2018\/TheBachelorette2018.png","esigor":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","motog6play":"MotorolaG62018\/MotorolaG62018.png","เชียร์แบบแมสๆ":"KbankxWorldcup\/KbankxWorldcup.png","человекмуравейиоса":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","お茶にしましょう":"cocacolaAyataka3\/cocacolaAyataka3.png","chopon":"atlantabraves2018\/atlantabraves2018.png","feriadehilos":"FeriaDelHilo\/FeriaDelHilo.png","سوا_لقدام":"HeroNextToHero_v3\/HeroNextToHero_v3.png","misfitsandmonsters":"truTV_Misfitsandmonsters\/truTV_Misfitsandmonsters.png","ibmer":"IBMThink2018_extension\/IBMThink2018_extension.png","stateofdecay2":"StateofDecay2\/StateofDecay2.png","amazonfindsaway":"JurassicWorld_FallenKingdom_AmazonFindsAWay\/JurassicWorld_FallenKingdom_AmazonFindsAWay.png","theopen":"TheOpen_2018\/TheOpen_2018.png","pubgmobile":"PubG_eSports_2018\/PubG_eSports_2018.png","halloweenmovies":"HalloweenMovie_2018\/HalloweenMovie_2018.png","panoramanyc":"PanoramaFestival_2018\/PanoramaFestival_2018.png","nyxl":"FranceBlizzardOWL_NY\/FranceBlizzardOWL_NY.png","halloweenmovie2018":"HalloweenMovie_2018\/HalloweenMovie_2018.png","masterchefbr":"MasterChefBR2018\/MasterChefBR2018.png","خلنا_نجتمع":"Vimto2018\/Vimto2018.png","nhs70":"NationalHealthService_70thAnniversary_v2\/NationalHealthService_70thAnniversary_v2.png","mmas2018":"MYXMusicAwards2018\/MYXMusicAwards2018.png","sharpobjects":"HBOSharpObjects\/HBOSharpObjects.png","バチェラー見てる人と語りたい":"BachelorJapanS2_v2\/BachelorJapanS2_v2.png","proudtobeabulldog":"NRLbulldogs2018\/NRLbulldogs2018.png","freshempire":"FreshEmpire_Q3_v2\/FreshEmpire_Q3_v2.png","alomãe":"BrazilWorldCup2018_AloMae_v3\/BrazilWorldCup2018_AloMae_v3.png","megザモンスター":"TheMeg_2018\/TheMeg_2018.png","فيمتو":"Vimto2018\/Vimto2018.png","إثراء_الرياضة":"ArabLeadersSummit2018_v4\/ArabLeadersSummit2018_v4.png","abrazosdegol":"ClaroPeru2018_v2\/ClaroPeru2018_v2.png","igor":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","gatsbyロールオン":"GatsbyDeo2018\/GatsbyDeo2018.png","hammerseries":"HammerSeries2018\/HammerSeries2018.png","heforshe":"HeForShe_fixed\/HeForShe_fixed.png","proudlysydney":"sydneyswans\/sydneyswans.png","askbtsxspotify":"SpotifyBTS2018_v2\/SpotifyBTS2018_v2.png","alômae":"BrazilWorldCup2018_AloMae_v3\/BrazilWorldCup2018_AloMae_v3.png","uberindia":"MoveForward_UberIndia_v2\/MoveForward_UberIndia_v2.png","綾鷹茶葉のあまみ":"cocacolaAyataka3\/cocacolaAyataka3.png","heladosextreme":"NestleExtreme_2018\/NestleExtreme_2018.png","uptheante":"FranceBlizzardOWL_Houston\/FranceBlizzardOWL_Houston.png","fortnitee3":"ForniteBattleRoyale2018\/ForniteBattleRoyale2018.png","vimto":"Vimto2018\/Vimto2018.png","เชียร์บอลโลก":"KbankxWorldcup\/KbankxWorldcup.png","poepraforasuascores":"BrazilNaturaAquarela\/BrazilNaturaAquarela.png","helloyou":"MotorolaG62018\/MotorolaG62018.png","ガチ勢の日":"GatsbyDeo2018\/GatsbyDeo2018.png","jointhehuddle":"AFLWestCoast\/AFLWestCoast.png","lasuertenojuega":"La_Suerte_No_Juega_v2\/La_Suerte_No_Juega_v2.png","powerkanan":"STARZPower_S5_Kanan\/STARZPower_S5_Kanan.png","三ツ矢サイダー":"Asahi_SoftDrinks_2018\/Asahi_SoftDrinks_2018.png","jeanchristopheetwinnie":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","cruzcampo":"Cruzcampo_2018\/Cruzcampo_2018.png","welcometowestworld":"HBOWestworld_Finale\/HBOWestworld_Finale.png","donthesash":"EssendonFC\/EssendonFC.png","whywewearblack":"TimesUp_v2\/TimesUp_v2.png","spotifyxbts":"SpotifyBTS2018_v2\/SpotifyBTS2018_v2.png","lgm":"NYMets2018\/NYMets2018.png","alienist":"TNT-Alienist\/TNT-Alienist.png","عطر_أبيات":"ArabianOud2018\/ArabianOud2018.png","beyourownchampion":"BeYourOwnChampion_WorldCup\/BeYourOwnChampion_WorldCup.png","walkonminks":"SuperflyMovie2018\/SuperflyMovie2018.png","heronexttohero":"HeroNextToHero_v3\/HeroNextToHero_v3.png","threelions":"ThreeLions2018\/ThreeLions2018.png","loveislandreunion":"LoveIsland2018_Flight3\/LoveIsland2018_Flight3.png","女のバトル":"BachelorJapanS2_v2\/BachelorJapanS2_v2.png","هي_وحدة":"Vimto2018\/Vimto2018.png","michaelmeyers":"HalloweenMovie_2018\/HalloweenMovie_2018.png","аквамен":"Aquaman_2018\/Aquaman_2018.png","colossus":"Deadpool2_Colossus\/Deadpool2_Colossus.png","キーラ":"StarWarsSolo_Qira\/StarWarsSolo_Qira.png","beersonus":"Clamato_2018\/Clamato_2018.png","ناس":"Flynas2018_v2\/Flynas2018_v2.png","roadtoberlin":"PubG_eSports_2018\/PubG_eSports_2018.png","wakandaforever":"BlackPantherHomeEnt2018\/BlackPantherHomeEnt2018.png","thenun":"TheNunMovie_2018\/TheNunMovie_2018.png","نوروز":"nowruz2018_v4\/nowruz2018_v4.png","ファンタビ":"fantasticbeasts_v3\/fantasticbeasts_v3.png","bringthemayhem":"FranceBlizzardOWL_Florida\/FranceBlizzardOWL_Florida.png","megtubarãogigante":"TheMeg_2018\/TheMeg_2018.png","blackhistorymonth":"BlackHistoryMonth\/BlackHistoryMonth.png","クリストファーロビン":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","와스프":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","superflymusic":"SuperflyMovie2018\/SuperflyMovie2018.png","namethatweekend":"Hotels_NameThatWeekend_2018\/Hotels_NameThatWeekend_2018.png","joguejunto":"BrazilWorldCup_JogueJunto_v3\/BrazilWorldCup_JogueJunto_v3.png","adoptadinosaur":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","dttvideo":"TroyeSivan_ArianaGrande_2018\/TroyeSivan_ArianaGrande_2018.png","loveloud":"ATT_TurnUpTheLove_v2\/ATT_TurnUpTheLove_v2.png","metoo":"MeToo_v3\/MeToo_v3.png","negasonic":"Deadpool2_Negasonic\/Deadpool2_Negasonic.png","thebachelorettefinale":"TheBachelorette2018\/TheBachelorette2018.png","wemetontwitter":"WeMetOnt_Emoji\/WeMetOnt_Emoji.png","rusiaentusmanos":"Telcel_RusiaEnTusManos_2018\/Telcel_RusiaEnTusManos_2018.png","maythe4thbewithyou":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","colonelhospital":"KFCGeneralHospital_v2\/KFCGeneralHospital_v2.png","niallhoranflicker":"NiallHoran2018\/NiallHoran2018.png","bestoftweet":"BestofTweets2018\/BestofTweets2018.png","championperformance":"BeYourOwnChampion_WorldCup\/BeYourOwnChampion_WorldCup.png","جيل_الذهب":"PepsiGoldenBoys_2018\/PepsiGoldenBoys_2018.png","jw2":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","mcdofries":"McDoPH_McDoFries_2018\/McDoPH_McDoFries_2018.png","puuh":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","vamoscomorgulho":"UberPride_Brasil_2018\/UberPride_Brasil_2018.png","エアアジアチャレンジ2018":"AirAsia2018_v2\/AirAsia2018_v2.png","arresteddevelopment":"ArrestedDevelopment2018\/ArrestedDevelopment2018.png","sexandthecity":"HBOSexandtheCity2018\/HBOSexandtheCity2018.png","ronstallworth":"BlackKlansmanMovie\/BlackKlansmanMovie.png","妖怪ウォッチワールド":"YokaiWatchWorld_Jibanyan\/YokaiWatchWorld_Jibanyan.png","itspooh":"ChristopherRobin_ItsPooh2018\/ChristopherRobin_ItsPooh2018.png","feelpretty":"feelpretty_v2\/feelpretty_v2.png","westworlds2":"HBOWestworld_Finale\/HBOWestworld_Finale.png","deadpool":"Deadpool2_Deadpool\/Deadpool2_Deadpool.png","animaisfantasticos":"fantasticbeasts_v3\/fantasticbeasts_v3.png","pepequenofilme":"WM_Smallfoot\/WM_Smallfoot.png","wearemanly":"NRLmanly2018\/NRLmanly2018.png","100simplejoysofdriving":"VW_SimpleJoysofDriving\/VW_SimpleJoysofDriving.png","antmanandwasp":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","lavidaesunpartido":"ChevroletMexico_WorldCup\/ChevroletMexico_WorldCup.png","lotmoreforlittlemore":"Vistara_2018\/Vistara_2018.png","shareacoke":"ShareACoke2018\/ShareACoke2018.png","jp25":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","atfr":"TheBachelorette2018\/TheBachelorette2018.png","신비한동물사전":"fantasticbeasts_v3\/fantasticbeasts_v3.png","thefourcomeback":"Fox_TheFour_Season2\/Fox_TheFour_Season2.png","neversettle":"Astros2018\/Astros2018.png","solomovie":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","ibm":"IBMThink2018_extension\/IBMThink2018_extension.png","デッドプール":"deadpooljapan18_v2\/deadpooljapan18_v2.png","sbi":"SBIBank_2018_Flight2\/SBIBank_2018_Flight2.png","bhm":"BlackHistoryMonth\/BlackHistoryMonth.png","powerghost":"STARZPower_S5_Ghost\/STARZPower_S5_Ghost.png","thewaspmovie":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","eyesonyou":"GOT7WORLDTOUR_2018\/GOT7WORLDTOUR_2018.png","くまのプーさん":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","loscrímenesdegrindelwald":"fantasticbeasts_v4\/fantasticbeasts_v4.png","звёздныевойны":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","vistaralove":"Vistara_2018\/Vistara_2018.png","newmotog":"MotorolaG62018\/MotorolaG62018.png","dinoday":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","esigór":"ChristopherRobin_Eeyore2018\/ChristopherRobin_Eeyore2018.png","exageranoexagero":"BrazilNaturaAquarela\/BrazilNaturaAquarela.png","nrl":"NRL2018\/NRL2018.png","pgi2018":"PubG_eSports_2018\/PubG_eSports_2018.png","jepa":"DirtIsGood_Persil\/DirtIsGood_Persil.png","whoisamerica":"ShowtimeQ3Program_2018\/ShowtimeQ3Program_2018.png","primeday18":"AmazonPrimeDay_2018\/AmazonPrimeDay_2018.png","thefirstfinals":"OverwatchLeague_WorldFinals_2018\/OverwatchLeague_WorldFinals_2018.png","랜도":"StarWarsSolo_Lando\/StarWarsSolo_Lando.png","pringlesacademy":"PringlesFrance_2018\/PringlesFrance_2018.png","camillepreaker":"HBOSharpObjects\/HBOSharpObjects.png","marvelstudiosantmanandthewasp":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","เชียร์ให้สุดหยุดที่บอลโลก":"KbankxWorldcup\/KbankxWorldcup.png","بطلة_جنب_بطل":"HeroNextToHero_v3\/HeroNextToHero_v3.png","mammamia2":"MammaMia2_v3\/MammaMia2_v3.png","castlerock":"Hulu_CastleRock_SinkingCar\/Hulu_CastleRock_SinkingCar.png","womeninfootball":"WomenInFootball2018_v2\/WomenInFootball2018_v2.png","herecomethegiants":"SuperNetball_HereComeTheGiants\/SuperNetball_HereComeTheGiants.png","bruxabrice":"BriceEmoji_2018\/BriceEmoji_2018.png","jurassicworld2":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","blacklivesmatter":"BlackHistoryMonth\/BlackHistoryMonth.png","ad5":"ArrestedDevelopment2018\/ArrestedDevelopment2018.png","piepequeño":"WM_Smallfoot\/WM_Smallfoot.png","paylikezlatan":"Visa_WorldCup2018_v2\/Visa_WorldCup2018_v2.png","pooh":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","fightingforglory":"FranceBlizzardOWL_Shanghai\/FranceBlizzardOWL_Shanghai.png","jurassicworldnight":"JurassicWorld_FallenKingdom_DinoDay_v2\/JurassicWorld_FallenKingdom_DinoDay_v2.png","westworldseason2":"HBOWestworld_Finale\/HBOWestworld_Finale.png","feriadelhilo":"FeriaDelHilo\/FeriaDelHilo.png","العربية_للعود":"ArabianOud2018\/ArabianOud2018.png","tdf2018":"TourDeFrance_2018\/TourDeFrance_2018.png","allcaps":"NHL_2017_2018_Caps_v3\/NHL_2017_2018_Caps_v3.png","eaststowin":"NRLRoosters2018\/NRLRoosters2018.png","tudopelaseleção":"GuaranaCopa_2018\/GuaranaCopa_2018.png","michaelmyers":"HalloweenMovie_2018\/HalloweenMovie_2018.png","シノアリス":"Sinoalice2018\/Sinoalice2018.png","じんめん犬":"YokaiWatchWorld_Jinmenken\/YokaiWatchWorld_Jinmenken.png","tigrão":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png","pantini":"PanteneInfluencer_2018\/PanteneInfluencer_2018.png","彦星":"StarFestivalDay_2018\/StarFestivalDay_2018.png","bronxnation":"NRLBroncos2018\/NRLBroncos2018.png","exploralodesconocido":"NestleExtreme_2018\/NestleExtreme_2018.png","inclusionishappening":"TwitterTogether_InclusionIsHappening_v2\/TwitterTogether_InclusionIsHappening_v2.png","animalesfantásticos":"fantasticbeasts_v3\/fantasticbeasts_v3.png","hilanderos":"FeriaDelHilo\/FeriaDelHilo.png","suerteono":"La_Suerte_No_Juega_v2\/La_Suerte_No_Juega_v2.png","ithra":"ArabLeadersSummit2018_v4\/ArabLeadersSummit2018_v4.png","yétietcompagnie":"WM_Smallfoot\/WM_Smallfoot.png","satc":"HBOSexandtheCity2018\/HBOSexandtheCity2018.png","تبرعك_أسهل":"ZamzamSociety2018\/ZamzamSociety2018.png","اقتصاد_الوقود":"SaudiEnergyEfficiencyCenter\/SaudiEnergyEfficiencyCenter.png","хрюня":"ChristopherRobin_Piglet2018\/ChristopherRobin_Piglet2018.png","lamonja":"TheNunMovie_2018\/TheNunMovie_2018.png","got7worldtour":"GOT7WORLDTOUR_2018\/GOT7WORLDTOUR_2018.png","كامل_الأوصاف":"NewChanganCar2018\/NewChanganCar2018.png","letsgopadres":"SDPadres2018\/SDPadres2018.png","バチェラー":"BachelorJapanS2_v2\/BachelorJapanS2_v2.png","antmanetlaguêpe":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","heretocreate":"Adidas_HereToCreate_WorldCup2018\/Adidas_HereToCreate_WorldCup2018.png","detroitsummers":"DetroitTigers2018\/DetroitTigers2018.png","jarir_deliver":"Jarir2018\/Jarir2018.png","스타워즈":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","thenunmovie":"TheNunMovie_2018\/TheNunMovie_2018.png","amazonfiretvcube":"FireTVLaunch2018\/FireTVLaunch2018.png","fastestfeet":"reebokflexweave_v2\/reebokflexweave_v2.png","handsfreetv":"FireTVLaunch2018\/FireTVLaunch2018.png","malibugames":"MalibuGamesSummer2018\/MalibuGamesSummer2018.png","ダブルウェアの出番":"EsteeLauder_DoubleWear\/EsteeLauder_DoubleWear.png","ittakesobsession":"TranssionTecno2018\/TranssionTecno2018.png","makethefuture":"Shell_MaketheFuture_2018\/Shell_MaketheFuture_2018.png","kohlscashsweepstakes":"KohlsCash_Q3_2018\/KohlsCash_Q3_2018.png","cmtaward":"CMTAwards2018_v2\/CMTAwards2018_v2.png","винни":"ChristopherRobin_Pooh2018\/ChristopherRobin_Pooh2018.png","discoverwestworld":"HBOWestworld_Finale\/HBOWestworld_Finale.png","madetofly":"SuperNetball_MadetoFly\/SuperNetball_MadetoFly.png","uberjourneys":"MoveForward_UberIndia_v2\/MoveForward_UberIndia_v2.png","gonswswifts":"SuperNetball_GoNSWSwifts\/SuperNetball_GoNSWSwifts.png","howwillyousurvive":"StateofDecay2_HowWillYouSurvive\/StateofDecay2_HowWillYouSurvive.png","askpanoramanyc":"PanoramaFestival_2018\/PanoramaFestival_2018.png","flywithadditve":"GEAdaptive_2018_v3\/GEAdaptive_2018_v3.png","dancetothispremiere":"TroyeSivan_ArianaGrande_2018\/TroyeSivan_ArianaGrande_2018.png","powertommy":"STARZPower_S5_Tommy\/STARZPower_S5_Tommy.png","africaemoji":"ABSA_2018_v2\/ABSA_2018_v2.png","torcedorfanático":"RexonaWorldCupEmoji\/RexonaWorldCupEmoji.png","boundbyblue":"AFLBoundbyBlue\/AFLBoundbyBlue.png","matriline":"A24_Hereditary2018\/A24_Hereditary2018.png","superhotdogger":"SuperHotdogger_2018\/SuperHotdogger_2018.png","lifefindsaway":"Jurassic_World_emoji_v3\/Jurassic_World_emoji_v3.png","قيمنا_معا":"MiskValues2018\/MiskValues2018.png","キリンレモン":"KirinLemon90thAnniversary_2018\/KirinLemon90thAnniversary_2018.png","갓세븐":"GOT7WORLDTOUR_2018\/GOT7WORLDTOUR_2018.png","raisedroyal":"kcroyals2018\/kcroyals2018.png","megderinlerdekidehset":"TheMeg_2018\/TheMeg_2018.png","raysup":"TampaBayRays2018\/TampaBayRays2018.png","weareraiders":"NRLraiders2018\/NRLraiders2018.png","maythe4th":"StarWarsSolo_Chewie_v2\/StarWarsSolo_Chewie_v2.png","voteparkhurst":"MLS_AllStarCaptains_Parkhurst\/MLS_AllStarCaptains_Parkhurst.png","بطل_جنب_بطله":"HeroNextToHero_v3\/HeroNextToHero_v3.png","everyonecancreate":"EveryoneCanCreate_v3\/EveryoneCanCreate_v3.png","truetotheblue":"SeattleMariners2018\/SeattleMariners2018.png","オレンジ文庫":"ShueishaBrand_2018_v4\/ShueishaBrand_2018_v4.png","superfly":"SuperflyMovie2018\/SuperflyMovie2018.png","honor10":"HuaweiHonorQ2GlobalLaunch_v2\/HuaweiHonorQ2GlobalLaunch_v2.png","lando":"StarWarsSolo_Lando\/StarWarsSolo_Lando.png","хансоло":"StarWarsSolo_HanSolo\/StarWarsSolo_HanSolo.png","bestneverrest":"MercedesGermany_BestNeverRest\/MercedesGermany_BestNeverRest.png","laguêpe":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","aceshigh":"FranceBlizzardOWL_London\/FranceBlizzardOWL_London.png","لنحياها":"MiskValues2018\/MiskValues2018.png","brose":"NationalRoseDay2018\/NationalRoseDay2018.png","persiannewyear":"nowruz2018_v4\/nowruz2018_v4.png","stlcards":"StLouisCardinals2018\/StLouisCardinals2018.png","satanicgrandmas":"A24_Hereditary2018\/A24_Hereditary2018.png","amazonprimeday":"AmazonPrimeDay_2018\/AmazonPrimeDay_2018.png","brosé":"NationalRoseDay2018\/NationalRoseDay2018.png","фантастическиетвари":"fantasticbeasts_v3\/fantasticbeasts_v3.png","flythenewfeeling":"Vistara_2018\/Vistara_2018.png","sachabaroncohen":"ShowtimeQ3Program_2018\/ShowtimeQ3Program_2018.png","clamatomichelada":"Clamato_2018\/Clamato_2018.png","lauriestrode":"HalloweenMovie_2018\/HalloweenMovie_2018.png","كن_سباقا_لعلاج_المرضى_الفقراء":"ZamzamSociety2018\/ZamzamSociety2018.png","whitesox":"whitesox2018\/whitesox2018.png","webringthunder":"SuperNetball_webringthunder\/SuperNetball_webringthunder.png","myvimto":"Vimto2018\/Vimto2018.png","yourodds":"WilliamHillWorldCup2018_v2\/WilliamHillWorldCup2018_v2.png","antmanylaavispa":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","birdland":"orioles2018_v2\/orioles2018_v2.png","pinstripepride":"NYYankees2018\/NYYankees2018.png","hilanderas":"FeriaDelHilo\/FeriaDelHilo.png","primeday2018":"AmazonPrimeDay_2018\/AmazonPrimeDay_2018.png","طيران_ناس":"Flynas2018_v2\/Flynas2018_v2.png","studentsstandup":"Parkland_Extension\/Parkland_Extension.png","megalodónpelícula":"TheMeg_2018_MegalodonPelicula\/TheMeg_2018_MegalodonPelicula.png","espejopúblico":"EspejoPublico_2017_2018\/EspejoPublico_2017_2018.png","كفاءة_الطاقة":"SaudiEnergyEfficiencyCenter\/SaudiEnergyEfficiencyCenter.png","thehaloway":"LAAngels2018\/LAAngels2018.png","masunidosquenunca":"CristalPeruMundial\/CristalPeruMundial.png","あなたの思いをそのまま聞かせて":"Adsforgood_Japan2018_v2\/Adsforgood_Japan2018_v2.png","marvelantmanandthewasp":"Disney_TheWasp_2018\/Disney_TheWasp_2018.png","votevaleri":"MLS_AllStarCaptains_Valeri\/MLS_AllStarCaptains_Valeri.png","afreirafilme":"TheNunMovie_2018\/TheNunMovie_2018.png","itstigger":"ChristopherRobin_Tigger2018\/ChristopherRobin_Tigger2018.png"},"profile_user":{"id":786939553,"id_str":"786939553","name":"Mars Weather","screen_name":"MarsWxReport","location":"Gale Crater, Mars","url":"http:\/\/mars.nasa.gov\/msl\/mission\/instruments\/environsensors\/rems\/","description":"Updates as avail from the REMS weather instrument aboard @MarsCuriosity.  Data credit: Centro deAstrobiologia, FMI, JPL\/NASA, Not an official acct.","protected":false,"followers_count":39016,"friends_count":47,"listed_count":305,"created_at":"Tue Aug 28 12:48:50 +0000 2012","favourites_count":216,"utc_offset":null,"time_zone":null,"geo_enabled":true,"verified":false,"statuses_count":1521,"lang":"en","contributors_enabled":false,"is_translator":false,"is_translation_enabled":false,"profile_background_color":"C0DEED","profile_background_image_url":"http:\/\/abs.twimg.com\/images\/themes\/theme1\/bg.png","profile_background_image_url_https":"https:\/\/abs.twimg.com\/images\/themes\/theme1\/bg.png","profile_background_tile":false,"profile_image_url":"http:\/\/pbs.twimg.com\/profile_images\/2552209293\/220px-Mars_atmosphere_normal.jpg","profile_image_url_https":"https:\/\/pbs.twimg.com\/profile_images\/2552209293\/220px-Mars_atmosphere_normal.jpg","profile_banner_url":"https:\/\/pbs.twimg.com\/profile_banners\/786939553\/1403835009","profile_link_color":"0084B4","profile_sidebar_border_color":"FFFFFF","profile_sidebar_fill_color":"DDEEF6","profile_text_color":"333333","profile_use_background_image":true,"has_extended_profile":false,"default_profile":false,"default_profile_image":false,"following":null,"follow_request_sent":null,"notifications":null,"business_profile_state":"none","translator_type":"none"},"profileEditingCSSBundle":"https:\/\/abs.twimg.com\/a\/1531883619\/css\/t1\/twitter_profile_editing.bundle.css","profile_id":786939553,"business_profile":false,"b2c_logged_out_support_indicators_enabled":true,"business_profile_featured_collections_complete":false,"cardsGallery":true,"injectComposedTweets":false,"inlineProfileEditing":false,"gdprSoftBounceEnabled":false,"isClusterFollowReplenishEnabled":false,"autoplayEnabled":true,"periscopeLiveStatusPollInterval":15000,"trendsCacheKey":null,"decider_personalized_trends":false,"trendsEndpoint":"\/i\/trends","wtfOptions":{"pc":true,"connections":true,"limit":3,"display_location":"profile-sidebar","dismissable":true,"similar_to_user_id":"786939553"},"showSensitiveContent":false,"autoPlayBalloonsAnimation":false,"momentsNuxTooltipsEnabled":false,"isCurrentUser":false,"isSensitiveProfile":false,"timeline_url":"\/i\/profiles\/show\/MarsWxReport\/timeline\/tweets","initialState":{"title":"Mars Weather (@MarsWxReport) | Twitter","section":null,"module":"app\/pages\/profile\/highline_landing","cache_ttl":300,"body_class_names":"three-col logged-out user-style-MarsWxReport enhanced-mini-profile ProfilePage ProfilePage--withWarning","doc_class_names":"route-profile","route_name":"profile","page_container_class_names":"AppContent","ttft_navigation":false}}'/>
      <input class="swift-boot-module" type="hidden" value="app/pages/profile/highline_landing"/>
      <input id="swift-module-path" type="hidden" value="https://abs.twimg.com/k/swift/en"/>
      <script async="" src="https://abs.twimg.com/k/en/init.en.3522ca3d1d205f226eb9.js">
      </script>
     </body>
    </html>
    
    


```python
# Get Mars Weather
mars_weather_list = []
for mars_weather in soup.find_all('p',class_= "TweetTextSize TweetTextSize--normal js-tweet-text tweet-text"):
    mars_weather_list.append(mars_weather.text.strip())

mars_weather = mars_weather_list[1]
print (mars_weather)

```

    Sol 2108 (2018-07-12), Sunny, high -24C/-11F, low -65C/-84F, pressure at 8.06 hPa, daylight 05:19-17:27
    


```python
#Scrape Mars Facts
# URL of page to be scraped 
url = 'https://space-facts.com/mars/'
```


```python
#Retrieve Fact Data from URL
mars_facts = pd.read_html(url)

#Create DataFrame
mars_facts_df = mars_facts[0]
mars_facts_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Equatorial Diameter:</td>
      <td>6,792 km</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Polar Diameter:</td>
      <td>6,752 km</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mass:</td>
      <td>6.42 x 10^23 kg (10.7% Earth)</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Moons:</td>
      <td>2 (Phobos &amp; Deimos)</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Orbit Distance:</td>
      <td>227,943,824 km (1.52 AU)</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Orbit Period:</td>
      <td>687 days (1.9 years)</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Surface Temperature:</td>
      <td>-153 to 20 °C</td>
    </tr>
    <tr>
      <th>7</th>
      <td>First Record:</td>
      <td>2nd millennium BC</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Recorded By:</td>
      <td>Egyptian astronomers</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Convert DataFrame to HTML
mars_facts_table = mars_facts_df.to_html(header=False, index=False)
print(mars_facts_table)
```

    <table border="1" class="dataframe">
      <tbody>
        <tr>
          <td>Equatorial Diameter:</td>
          <td>6,792 km</td>
        </tr>
        <tr>
          <td>Polar Diameter:</td>
          <td>6,752 km</td>
        </tr>
        <tr>
          <td>Mass:</td>
          <td>6.42 x 10^23 kg (10.7% Earth)</td>
        </tr>
        <tr>
          <td>Moons:</td>
          <td>2 (Phobos &amp; Deimos)</td>
        </tr>
        <tr>
          <td>Orbit Distance:</td>
          <td>227,943,824 km (1.52 AU)</td>
        </tr>
        <tr>
          <td>Orbit Period:</td>
          <td>687 days (1.9 years)</td>
        </tr>
        <tr>
          <td>Surface Temperature:</td>
          <td>-153 to 20 °C</td>
        </tr>
        <tr>
          <td>First Record:</td>
          <td>2nd millennium BC</td>
        </tr>
        <tr>
          <td>Recorded By:</td>
          <td>Egyptian astronomers</td>
        </tr>
      </tbody>
    </table>
    


```python
executable_path = {'executable_path': 'chromedriver.exe'}
browser = Browser('chrome', **executable_path, headless=False)
```


```python
url = 'https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars'
browser.visit(url)
```


```python
# Get the URL for the Full Image of the Featured Space Image
html = browser.html
```


```python
# Create BeautifulSoup object; parse with 'html.parser'
soup = BeautifulSoup(html, 'html.parser')
```


```python
# Examine the results, then determine element that contains sought info
print(soup.prettify())
```

    <!DOCTYPE html>
    <html lang="en" xmlns="http://www.w3.org/1999/xhtml">
     <head>
      <link href="//ajax.googleapis.com/ajax/libs/jqueryui/1.11.3/themes/smoothness/jquery-ui.css" rel="stylesheet" type="text/css"/>
      <script async="" src="https://ssl.google-analytics.com/ga.js" type="text/javascript">
      </script>
      <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js" type="text/javascript">
      </script>
      <title>
       Astropedia Search Results | USGS Astrogeology Science Center
      </title>
      <meta content="USGS Astrogeology Science Center Astropedia search results." name="description"/>
      <meta content="USGS,Astrogeology Science Center,Cartography,Geology,Space,Geological Survey,Mapping" name="keywords"/>
      <meta content="IE=edge" http-equiv="X-UA-Compatible"/>
      <meta content="text/html; charset=utf-8" http-equiv="Content-Type"/>
      <meta content="width=device-width, initial-scale=1, maximum-scale=1" name="viewport"/>
      <meta content="x61hXXVj7wtfBSNOPnTftajMsZ5yB2W-qRoyr7GtOKM" name="google-site-verification"/>
      <!--<link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Open+Sans:400italic,400,bold"/>-->
      <link href="/css/main.css" media="screen" rel="stylesheet"/>
      <link href="/css/print.css" media="print" rel="stylesheet"/>
      <!--[if lt IE 9]>
    			<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    			<script src="/js/respond.min.js"></script>
    			<link rel="stylesheet" type="text/css" href="/css/ie.css"/>
                            <script>
                              document.createElement('header');
                              document.createElement('nav');
                              document.createElement('section');
                              document.createElement('article');
                              document.createElement('aside');
                              document.createElement('footer');
                              document.createElement('hgroup');
                            </script>
                      <![endif]-->
      <link href="/favicon.ico" rel="icon" type="image/x-ico"/>
     </head>
     <body id="results">
      <header>
       <h1>
        Astrogeology Science Center
       </h1>
       <a href="http://www.usgs.gov">
        <img alt="USGS: Science for a Changing World" class="logo" height="70" src="/images/usgs_logo_main_2x.png" width="180"/>
       </a>
      </header>
      <div class="wrapper">
       <nav>
        <a href="#" id="nav-toggle" title="Navigation Menu">
         Menu
        </a>
        <ul class="dropdown dropdown-horizontal" id="yw0">
         <li>
          <a href="/">
           Home
          </a>
         </li>
         <li>
          <a href="/about">
           About
          </a>
          <ul>
           <li>
            <a href="/about/careers">
             Careers
            </a>
           </li>
           <li>
            <a href="/contact">
             Contact
            </a>
           </li>
           <li>
            <a href="/about/events">
             Events
            </a>
           </li>
           <li>
            <a href="/site/glossary">
             Glossary
            </a>
           </li>
           <li>
            <a href="/about/mission">
             Mission
            </a>
           </li>
           <li>
            <a href="/news">
             News
            </a>
           </li>
           <li>
            <a href="/people">
             People
            </a>
           </li>
           <li>
            <a href="/about/using-our-images">
             Using Our Images
            </a>
           </li>
           <li>
            <a href="/about/visitors">
             Visitors
            </a>
           </li>
          </ul>
         </li>
         <li>
          <a href="/facilities">
           Labs / Facilities
          </a>
          <ul>
           <li>
            <a href="/facilities/flynn-creek-crater-sample-collection">
             Flynn Creek Crater Sample Collection
            </a>
           </li>
           <li>
            <a href="http://www.moon-cal.org">
             Lunar Calibration Project
            </a>
           </li>
           <li>
            <a href="/facilities/meteor-crater-sample-collection">
             Meteor Crater Sample Collection
            </a>
           </li>
           <li>
            <a href="/facilities/mrctr">
             MRCTR GIS Lab
            </a>
           </li>
           <li>
            <a href="/facilities/cartography-and-imaging-sciences-node-of-nasa-planetary-data-system">
             PDS Cartography and Imaging Sciences Node
            </a>
           </li>
           <li>
            <a href="/pds/annex">
             PDS IMG Annex
            </a>
           </li>
           <li>
            <a href="/facilities/photogrammetry-guest-facility">
             Photogrammetry Guest Facility
            </a>
           </li>
           <li>
            <a href="/rpif">
             Regional Planetary Information Facility (RPIF)
            </a>
           </li>
          </ul>
         </li>
         <li>
          <a href="/maps">
           Maps / Products
          </a>
          <ul>
           <li>
            <a href="/search">
             Product Search
            </a>
           </li>
           <li>
            <a href="http://planetarynames.wr.usgs.gov">
             Gazetteer of Planetary Nomenclature
            </a>
           </li>
           <li>
            <a href="http://planetarymapping.wr.usgs.gov">
             Geologic Mapping Program
            </a>
           </li>
           <li>
            <a href="http://pilot.wr.usgs.gov">
             Planetary Image Locator Tool (PILOT)
            </a>
           </li>
           <li>
            <a href="/search/planetary-index">
             Planetary Map Index
            </a>
           </li>
          </ul>
         </li>
         <li>
          <a href="/geology">
           Missions / Research
          </a>
          <ul>
           <li>
            <a href="/geology/mars-dunes">
             Mars Dunes
            </a>
           </li>
           <li>
            <a href="/geology/mars-ice">
             Mars Ice
            </a>
           </li>
           <li>
            <a href="/missions">
             Mission Support
            </a>
           </li>
           <li>
            <a href="/solar-system">
             Solar System
            </a>
           </li>
           <li>
            <a href="/groups">
             Working Groups
            </a>
           </li>
          </ul>
         </li>
         <li>
          <a href="/tools">
           Tools
          </a>
          <ul>
           <li>
            <a href="http://planetarynames.wr.usgs.gov">
             Gazetteer of Planetary Nomenclature
            </a>
           </li>
           <li>
            <a href="http://isis.astrogeology.usgs.gov">
             Integrated Software for Imagers and Spectrometers (ISIS)
            </a>
           </li>
           <li>
            <a href="http://astrogeology.usgs.gov/tools/map-a-planet-2">
             Map a Planet 2
            </a>
           </li>
           <li>
            <a href="http://pilot.wr.usgs.gov">
             Planetary Image Locator Tool (PILOT)
            </a>
           </li>
           <li>
            <a href="http://astrocloud.wr.usgs.gov/">
             Projection on the Web (POW)
            </a>
           </li>
          </ul>
         </li>
        </ul>
        <form action="/search/results" class="search" id="search" method="get">
         <input title="Search Astropedia" type="submit" value=""/>
         <input name="q" placeholder="Search" type="text"/>
         <input name="__ncforminfo" type="hidden" value="nQ6u4KVhRgaMQuoXukXip3lHwwGgg-WqHyBoN9WEnczR0TJiyYdsJif_zKCdGp0vK7WLnGpQX2VcRuL5NlUMdIuAcya2_JcFGtTQAvU2FrE="/>
        </form>
       </nav>
       <div class="container">
        <form action="/search/results" class="bar widget block" id="search-bar">
         <input name="q" type="hidden" value="hemisphere-enhanced"/>
         <input name="target" type="hidden" value="Mars"/>
         <input name="__ncforminfo" type="hidden" value="nQ6u4KVhRgaMQuoXukXip3lHwwGgg-WqHyBoN9WEncyZAU3lyRmnJsVnxqwKUbT8gVB5EnKQ0ZPBrEgB20F1VjEo0XjuoLVUXgl6MjesUAiasi76UxwNCg=="/>
        </form>
        <div class="full-content">
         <section class="block" id="results-accordian">
          <div class="result-list" data-section="product" id="product-section">
           <div class="accordian">
            <h2>
             Products
            </h2>
            <span class="count">
             4 Results
            </span>
            <span class="collapse">
             Collapse
            </span>
           </div>
           <div class="collapsible results">
            <div class="item">
             <a class="itemLink product-item" href="/search/map/Mars/Viking/cerberus_enhanced">
              <img alt="Cerberus Hemisphere Enhanced thumbnail" class="thumb" src="/cache/images/dfaf3849e74bf973b59eb50dab52b583_cerberus_enhanced.tif_thumb.png"/>
             </a>
             <div class="description">
              <a class="itemLink product-item" href="/search/map/Mars/Viking/cerberus_enhanced">
               <h3>
                Cerberus Hemisphere Enhanced
               </h3>
              </a>
              <span class="subtitle" style="float:left">
               image/tiff 21 MB
              </span>
              <span class="pubDate" style="float:right">
              </span>
              <br/>
              <p>
               Mosaic of the Cerberus hemisphere of Mars projected into point perspective, a view similar to that which one would see from a spacecraft. This mosaic is composed of 104 Viking Orbiter images acquired…
              </p>
             </div>
             <!-- end description -->
            </div>
            <div class="item">
             <a class="itemLink product-item" href="/search/map/Mars/Viking/schiaparelli_enhanced">
              <img alt="Schiaparelli Hemisphere Enhanced thumbnail" class="thumb" src="/cache/images/7677c0a006b83871b5a2f66985ab5857_schiaparelli_enhanced.tif_thumb.png"/>
             </a>
             <div class="description">
              <a class="itemLink product-item" href="/search/map/Mars/Viking/schiaparelli_enhanced">
               <h3>
                Schiaparelli Hemisphere Enhanced
               </h3>
              </a>
              <span class="subtitle" style="float:left">
               image/tiff 35 MB
              </span>
              <span class="pubDate" style="float:right">
              </span>
              <br/>
              <p>
               Mosaic of the Schiaparelli hemisphere of Mars projected into point perspective, a view similar to that which one would see from a spacecraft. The images were acquired in 1980 during early northern…
              </p>
             </div>
             <!-- end description -->
            </div>
            <div class="item">
             <a class="itemLink product-item" href="/search/map/Mars/Viking/syrtis_major_enhanced">
              <img alt="Syrtis Major Hemisphere Enhanced thumbnail" class="thumb" src="/cache/images/aae41197e40d6d4f3ea557f8cfe51d15_syrtis_major_enhanced.tif_thumb.png"/>
             </a>
             <div class="description">
              <a class="itemLink product-item" href="/search/map/Mars/Viking/syrtis_major_enhanced">
               <h3>
                Syrtis Major Hemisphere Enhanced
               </h3>
              </a>
              <span class="subtitle" style="float:left">
               image/tiff 25 MB
              </span>
              <span class="pubDate" style="float:right">
              </span>
              <br/>
              <p>
               Mosaic of the Syrtis Major hemisphere of Mars projected into point perspective, a view similar to that which one would see from a spacecraft. This mosaic is composed of about 100 red and violet…
              </p>
             </div>
             <!-- end description -->
            </div>
            <div class="item">
             <a class="itemLink product-item" href="/search/map/Mars/Viking/valles_marineris_enhanced">
              <img alt="Valles Marineris Hemisphere Enhanced thumbnail" class="thumb" src="/cache/images/04085d99ec3713883a9a57f42be9c725_valles_marineris_enhanced.tif_thumb.png"/>
             </a>
             <div class="description">
              <a class="itemLink product-item" href="/search/map/Mars/Viking/valles_marineris_enhanced">
               <h3>
                Valles Marineris Hemisphere Enhanced
               </h3>
              </a>
              <span class="subtitle" style="float:left">
               image/tiff 27 MB
              </span>
              <span class="pubDate" style="float:right">
              </span>
              <br/>
              <p>
               Mosaic of the Valles Marineris hemisphere of Mars projected into point perspective, a view similar to that which one would see from a spacecraft. The distance is 2500 kilometers from the surface of…
              </p>
             </div>
             <!-- end description -->
            </div>
            <script>
             addBases=[];;if(typeof resetLayerSwitcher==="function"){resetLayerSwitcher(false)};var productTotal = 4;
            </script>
           </div>
           <!-- end this-section -->
          </div>
         </section>
        </div>
       </div>
       <div class="icons projects black scroll-wrapper">
        <div class="scroll">
         <a class="icon" href="http://isis.astrogeology.usgs.gov" title="Integrated Software for Imagers and Spectrometers">
          <img alt="ISIS Logo" height="112" src="/images/logos/isis_2x.jpg" width="112"/>
          <span class="label">
           ISIS
          </span>
         </a>
         <a class="icon" href="http://planetarynames.wr.usgs.gov" title="Gazetteer of Planetary Nomenclature">
          <img alt="Nomenclature Logo" height="112" src="/images/logos/nomenclature_2x.jpg" width="112"/>
          <span class="label">
           Planetary Nomenclature
          </span>
         </a>
         <a class="icon" href="http://astrogeology.usgs.gov/tools/map" title="Map a Planet 2">
          <img alt="Map-a-Planet Logo" height="112" src="/images/logos/map_a_planet_2x.jpg" width="112"/>
          <span class="label">
           Map a Planet 2
          </span>
         </a>
         <a class="icon" href="/facilities/imaging-node-of-nasa-planetary-data-system-pds" title="PDS Imaging Node">
          <img alt="PDS Logo" height="112" src="/images/pds_logo-black-web.png"/>
          <span class="label">
           PDS Imaging Node
          </span>
         </a>
         <!--
    						<a title="Astropedia Search" href="/search" class="icon">
    							<img alt="Astropedia Logo" height="112" width="112" src="/images/logos/astropedia_2x.jpg"/>
    							<span class="label">Astropedia</span>
    						</a>
    -->
         <a class="icon" href="/rpif" title="Regional Planetary Image Facility">
          <img alt="RPIF Logo" height="112" src="/images/logos/rpif_2x.jpg" width="112"/>
          <span class="label">
           RPIF
          </span>
         </a>
         <a class="icon" href="/facilities/photogrammetry-guest-facility" title="Photogrammetry Guest Facility">
          <img alt="Photogrammetry Guest Faciltiy Logo" height="112" src="/images/logos/photogrammetry_2x.jpg" width="112"/>
          <span class="label">
           Photogrammetry Guest Facility
          </span>
         </a>
         <a class="icon" href="http://pilot.wr.usgs.gov" title="Planetary Image Locator Tool">
          <img alt="Pilot Logo" height="112" src="/images/logos/pilot_2x.jpg" width="112"/>
          <span class="label">
           PILOT
          </span>
         </a>
         <a class="icon" href="/facilities/mrctr" title="Mapping, Remote-sensing, Cartography, Technology and Research GIS Lab">
          <img alt="MRCTR GIS Lab Logo" height="112" src="/images/logos/mrctr_2x.jpg" width="112"/>
          <span class="label">
           MRCTR GIS Lab
          </span>
         </a>
        </div>
       </div>
       <footer>
        <div class="left">
         <a href="http://astrogeology.usgs.gov">
          Home
         </a>
         |
         <a href="http://astrogeology.usgs.gov/contact">
          Contact
         </a>
         |
         <a href="http://astrogeology.usgs.gov/about/events">
          Events
         </a>
         |
         <a href="http://astrogeology.usgs.gov/news">
          News
         </a>
        </div>
        <div class="right">
         <a href="http://www.doi.gov">
          U.S. Department of Interior
         </a>
         |
         <a href="http://www.usgs.gov">
          U.S. Geological Survey
         </a>
         |
         <a href="http://www.usa.gov">
          USA.gov
         </a>
        </div>
       </footer>
      </div>
      <!--
    		<div class="credit">
    			<small>Background Credits: NASA/USGS</small>
    		</div>
    -->
      <div class="page-background" style="
    			background:url('/images/backgrounds/mars.jpg');
    			filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(
    				src='/images/backgrounds/mars.jpg', sizingMethod='scale');
    		">
      </div>
      <script type="text/javascript">
       var baseUrl = "";
    
    
    var _gaq = _gaq || [];_gaq.push(['_setAccount', 'UA-27613186-1']);_gaq.push(['_trackPageview']);(function() { var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js'; var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);})();
      </script>
      <script src="//ajax.googleapis.com/ajax/libs/jqueryui/1.11.3/jquery-ui.min.js" type="text/javascript">
      </script>
      <script src="/js/general.js" type="text/javascript">
      </script>
     </body>
    </html>
    


```python
#Get the four product images

first_product = browser.find_by_tag('h3')[0].text
second_product = browser.find_by_tag('h3')[1].text
third_product = browser.find_by_tag('h3')[2].text
fourth_product = browser.find_by_tag('h3')[3].text

#Get the four product urls
browser.find_by_css('.thumb')[0].click()
first_prod_img = browser.find_by_text('Sample')['href']
browser.back()

browser.find_by_css('.thumb')[1].click()
second_prod_img = browser.find_by_text('Sample')['href']
browser.back()

browser.find_by_css('.thumb')[2].click()
third_prod_img = browser.find_by_text('Sample')['href']
browser.back()

browser.find_by_css('.thumb')[3].click()
fourth_prod_img = browser.find_by_text('Sample')['href']
browser.back()

hemisphere_images=[{'title':first_product, 'hem_url': first_prod_img},
                   {'title':second_product,'hem_url': second_prod_img},
                   {'title':third_product, 'hem_url': third_prod_img},
                   {'title':fourth_product,'hem_url':fourth_prod_img}]

print(hemisphere_images)
    
```

    [{'title': 'Cerberus Hemisphere Enhanced', 'hem_url': 'http://astropedia.astrogeology.usgs.gov/download/Mars/Viking/cerberus_enhanced.tif/full.jpg'}, {'title': 'Schiaparelli Hemisphere Enhanced', 'hem_url': 'http://astropedia.astrogeology.usgs.gov/download/Mars/Viking/schiaparelli_enhanced.tif/full.jpg'}, {'title': 'Syrtis Major Hemisphere Enhanced', 'hem_url': 'http://astropedia.astrogeology.usgs.gov/download/Mars/Viking/syrtis_major_enhanced.tif/full.jpg'}, {'title': 'Valles Marineris Hemisphere Enhanced', 'hem_url': 'http://astropedia.astrogeology.usgs.gov/download/Mars/Viking/valles_marineris_enhanced.tif/full.jpg'}]
    


```python
browser.quit()
```
