# KeyBoardSticky
Extension for simplify the use of a view that should stick to the key board when appeared.

How to use:
 
 Your UIViewController should conform to 'IKeyBoardSticky'
 
 You should to implement:

   NotificationCenter.default.addObserver(self, selector: #selector(keyboardFrameChanged(notification:)), name:    NSNotification.Name.UIKeyboardWillChangeFrame, object: nil)
   NotificationCenter.default.addObserver(self, selector: #selector(keyboardWillShow(notification:)), name:   NSNotification.Name.UIKeyboardWillShow, object: nil)
   NotificationCenter.default.addObserver(self, selector: #selector(keyboardWillHide(notification:)), name:   NSNotification.Name.UIKeyboardWillHide, object: nil)
 
 And call "keyBoardChangeNotif" on all results.
 
 After calculation you will be fired back on function 'heightFromBottomOfScreenToKeyBoardTopChange' the new height, with animation params.
 
 Don't forget to unsebsribe NotificationCenter
