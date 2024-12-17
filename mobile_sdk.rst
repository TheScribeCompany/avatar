1. Mobile SDK
===============

.. figure:: _static/images/WEBSOCKET_SDK_Workflow.png

   :alt: 

1. **Registration**: Businesses must provide their unique business Id and email to register with Avatar. This data is stored in DynamoDB database. 

2. **SDK integration**: Depending on the platforms, businesses can use Web SDK to integrate into the website. If it is to be integrated into a mobile app, then there are 2 SDKs. One is in Java and the other is in React Native SDK. So, depending on the business requirements, either of them can be used. 

3. **Connection with WebSocket**: The business first creates a connection with Avatar's WebSocket Server which is a Node Server that is handled by Vodal by sending business Id and email.  

4. **Returns Unique Connection ID**: After receiving the details, the server will create a unique ID against the business entry in Neptune, different database table altogether. It returns a unique connection ID (which is a system generated email) to the website or mobile. 

5. **QR code/Deep Link generation**: For Web users, a QR code is sent with the unique connection ID for users to scan. Whereas for mobile users, a deep link URL is sent.  
   Once the user scans the QR code or clicks on deep link URL, the Avatar app connects to WebSocket Server and shares unique connection ID to validate user's identity. 

6. **Email selection**: Now, to associate with Avatar account, the user can select an existing email (like Google, Microsoft, or in-house OTP verified email) or proxy email provided by Avatar. 

7. **Update WebSocket with more details**: The unique ID, customer email, FCM token (notifications) are sent along and stored in DynamoDB through WebSocket connection. 

8. **Notification**: Avatar sends a confirmation notification to the device through the Avatar app showing successful sign-up,
   and on the other hand the user email is sent to the business connection showing "success state".
   Once registered, the business can communicate with the user using the user's chosen email or a proxy email. 