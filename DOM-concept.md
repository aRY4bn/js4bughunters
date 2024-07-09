DOM => Document Object Model 

 -HTML => Static 
 -DOM => api 
JS use api(DOM) to connect with HTML
یک api است که باعث ارتباط js با html صفحه می شود .
در واقع تمام تگ ها و کد های html به صورت document در js ذخیره می شود و js با DOM می تواند به آن دسترسی داشته باشد.
در واقع DOM فایل هایی با پسوند html و xml را می گیرد و به یک object تبدیل می کند که js بتواند آن را بشناسد.
در واقع تگ ها در html به صورت element در js شناخته میشود




CRP => Critical Rendering Path
در واقع هر browser برای خود یک CRP دارد که بر اساس اولویت آن مشخص می کند که کدام بخش صفحه ابتدا رندر گرفته شود.

DOM : Spource & Sink
*DOM Source => وقتی کاربر اطلاعات را در سایت وارد میکند در این قسمت می نشیند 
  - document.url
  - location.hash 
  - xhr.responseText

*DOM Sink => محلی است که ورودی کاربر اجرا می شود
  - document.write()
  - innerHTML
  - postMessage
