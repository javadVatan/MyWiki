----------------------------------------------------------------- Copy a Text -------------------------------------------------------------------------------------
 
 const el = document.createElement('textarea');
  el.value = 'Text to copy';
  el.setAttribute('readonly', '');
  el.style.position = 'absolute';
  el.style.left = '-9999px';
  document.body.appendChild(el);
  el.select();
  document.execCommand('copy');
  document.body.removeChild(el); 
  
  
  ----------------------------------------------------------------- Search for links -------------------------------------------------------------------------------------
   var arr = [], l = document.links;
    for(var i=0; i<l.length; i++) {
      arr.push(l[i].href);
    }
   console.log(arr)
   
   
   ------------------------------------------- Copy all .*** links from page -------------------------------------------------------------
  var arr = '', l = document.links;
    for(var i=0; i<l.length; i++) {
        const value = l[i].toString()
        if(value.includes('.***'))
          arr += l[i].href+', ';
    }
  const el = document.createElement('textarea');
  el.value =arr;
  el.setAttribute('readonly', '');
  el.style.position = 'absolute';
  el.style.left = '-9999px';
  document.body.appendChild(el);
  el.select();
  document.execCommand('copy');
  document.body.removeChild(el);
