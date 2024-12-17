2. Authentication API
======================

In the Avatar app, authentication API allows decentralized, biometric based user authentication to ensure secure access without storing personal data. 
Every user's immutable biometric factor results in unique identity. These identities are transformed into cryptographic keys which are anonymous, portable, and revokable. 
This identity system operator, Avatar Inc, will never have access to user's personal information. 
This kind of decentralized model makes sure that users have access to self-sovereign identity wallet securely and are given full control over identity verification
without data being exposed.  Since Avatar is focused on privacy-first principles, authentication mechanisms often emphasize strong security and privacy controls, 
protecting user data and ensuring that only authorized individuals can access and manage their digital identities. 

.. raw:: html

 <hr style="border: 1px solid #ccc; margin: 20px 0;">


.. code-block:: json




    {
        "auths": 
        [
            {
                "customerBizId": "did:avtr:5atqQC8JCCgKxN9XpiQxKs",
                "businessId": "ZjUxODNmYTI3NDczOWYzNjRmZTI0NjBhMzdmMWYzYTM6OlQxZS94Y1l1TGhqdGl4bXpkeFl0VXc9PQ==",
                "method": "biometric",
                "appAction": "authentication",
                "success": true
            }
        ]
    }



.. raw:: html

 <hr style="border: 1px solid #ccc; margin: 20px 0;">


**Attributes**

+-------------------+-------------------+--------------------------------------------------------------------------+
| Fields            | Type              | Description                                                              |
+===================+===================+==========================================================================+
| customerBizId     | String            | Unique connection Id sent by WebSocket server against the business entry |
+-------------------+-------------------+--------------------------------------------------------------------------+
| BusinessId        | String            | Unique Id of the business                                                |
+-------------------+-------------------+--------------------------------------------------------------------------+
| method            | String            | Takes user's live face for authentication                                |
+-------------------+-------------------+--------------------------------------------------------------------------+
| appAction         | String            | What kind of action is being taken                                       |
+-------------------+-------------------+--------------------------------------------------------------------------+
| success           | String            | Checks authentication is successful or not                               |
+-------------------+-------------------+--------------------------------------------------------------------------+

.. raw:: html

 <hr style="border: 1px solid #ccc; margin: 20px 0;">
 

.. raw:: html

   <link rel="stylesheet" href="custom.css">
   <script src="custom.js"></script>
   
   <!-- Container for tab buttons -->
       <div class="tablink-container">
       <button class="tablink" onclick="openTab(event, 'Tab1')">JSON</button>
       <button class="tablink" onclick="openTab(event, 'Tab2')">Python</button>
       </div>

       <!-- Tab 1 content -->
       <div id="Tab1" class="tabcontent">
           <h3>code-block</h3>
           <pre>
   {
       "auths": [
           {
               "customerBizId": "did:avtr:5atqQC8JCCgKxN9XpiQxKs",
               "businessId": "ZjUxODNmYTI3NDczOWYzNjRmZTI0NjBhMzdmMWYzYTM6OlQxZS94Y1l1TGhqdGl4bXpkeFl0VXc9PQ==",
               "method": "biometric",
               "appAction": "authentication",
               "success": true
           }
       ]
   }
           </pre>
           <button class="copy-button" onclick="copyCode()">Copy</button>
       </div>

       <!-- Tab 2 content -->
       <div id="Tab2" class="tabcontent">
           <h3>code-block</h3>
           <p>This is the content inside Tab 2.</p>
           <button class="copy-button" onclick="copyCode()">Copy</button>
       </div>
   


.. raw:: html

 <hr style="border: 1px solid #ccc; margin: 20px 0;">

.. raw:: html

    <div class="dropdown">
        <button class="dropdown-button">Select an Option</button>
        <div class="dropdown-content">
            <a href="#" onclick="showContent('content1')">Option 1</a>
            <a href="#" onclick="showContent('content2')">Option 2</a>
            <a href="#" onclick="showContent('content3')">Option 3</a>
        </div>
    </div>

    <!-- Content container -->
    <div id="dynamic-content">
        <div id="content1" class="content-item" style="display: none;">
            <p>This is where you add the content for the first option. You can include text, images, or even additional HTML elements.
        </div>
        <div id="content2" class="content-item" style="display: none;">
            <p>This is the content for Option 2.</p>
        </div>
        <div id="content3" class="content-item" style="display: none;">
            <p>This is the content for Option 3.</p>
        </div>
    </div>







