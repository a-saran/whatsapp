# whatsapp
whatsapp message script

 * Open whatsapp web
 * Open the target person chat
 * Run the code in console


```js
(function() {
  var TimeInternal = 2000; //2 seconds
  var message = 'message you want to send'; // message
  var messgeCount = 100; //messageCount

  var eventFire = (MyElement, ElementType) => { 
    var MyEvent = document.createEvent("MouseEvents"); 
    MyEvent.initMouseEvent 
     (ElementType, true, true, window, 0, 0, 0, 0, 0, false, false, false, false, 0, null); 
    MyElement.dispatchEvent(MyEvent); 
  }; 
  var i = 1;
  var id = setInterval(function(){
  if(i < messgeCount) {
    window.InputEvent = window.Event || window.InputEvent;
    var inputEvent = new InputEvent('input', {bubbles: true});
    var textbox= document.querySelector('#main > footer .copyable-text.selectable-text');
    textbox.textContent = message;
    textbox.dispatchEvent(inputEvent);
    eventFire(document.querySelector('span[data-icon="send"]'), 'click');
    i = i + 1;
  }else {
    clearInterval(id);
  }
  }, TimeInternal)
})()
```
