1. Registration API
====================

Registration is the process where a new user creates an account to establish their self-sovereign identity. 
During registration, users typically provide necessary information and set up authentication credentials (such as a password or biometric data) to securely access the app. 
This initial setup may also involve verifying their identity to ensure that only authorized individuals can create a unique, 
privacy-first digital identity wallet within the Avatar ecosystem. 
This registration process lays the foundation for users to securely manage their personal data and identity within the app. 


.. .. raw:: html


..   <div class="page-split">
..    <div class="left">
..       <p>A Registration API is a service endpoint that allows users or systems to securely create and register accounts or resources within an application or platform. 
           It plays a critical role in user onboarding, facilitating seamless integration and authentication processes.</p>
..    </div>
..    <div class="right">
        <p>Here is the code block:</p>
..    </div>
..   </div>


.. raw:: html

 <hr style="border: 1px solid #ccc; margin: 20px 0;"> 


.. code-block:: json




    { 
  "auths": [ 
    { 
          "customerBizId": "did:avtr:5atqQC8JCCgKxN9XpiQxKs", 
          "token": "ZWFjZDAxYzkxMjc1NTdlYWM0NzA4ODNjNzUxMWQ4NGM6OjNQeE9nc3c2aUEzT1RnTWhRVWVZZlN1dVVJOTFwR0YyZGVUTnJtVzhENmM9", 
          "faceKey": { 
    "localProfiles": [ 
        { 
            "person": { 
                "version-number": 0.1, 
                "serialNumber": "50ac875f-cda9-2e87-ab44-d23b6c46428f", 
                "subjectID": "48bd02d5-eb8f-8571-689b-caa07fac6436", 
                "inheritsFrom": "", 
                "subjectPublicKey": { 
                    "coseID": -7, 
                    "keyValue": "04:8b:bd:66:39:55:05:09:97:9b:bd:bc:66:e8:ac:af:e8:c5:ec:5c:2b:5a:f5:f4:65:0f:38:73:3d:c8:f7:06:2f:94:22:29:f4:48:ed:0c:95:dd:5d:6e:6e:21:9f:b1:37:61:be:be:82:c8:25:8c:a2:75:3e:7c:d8:79:84:d5:1c" 
                }, 
                "validity": { 
                    "notBefore": 1704097193000, 
                    "notAfter": 1717226393000 
                }, 
                "subjectConsentObtained": true, 
                "assignedTo": "bed8abba-92dd-cff8-b268-a9e4dd6945ca", 
                "verificationData": "/KO0xRoY4kFm2VjUToMb5etnh4dnrzWUEI8pbX/mo6M=", 
                "extensions": [ 
                    { 
                        "type": "privateData", 
                        "version": 0.2, 
                        "content": "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" 
                    },
                    { 
                        "type": "useRestriction", 
                        "version": 0.5, 
                        "content": "K+FZTRtLV4UtZxNOKflMSQMuw93zzhfPieKRVFAoatpw2D47/9HYkkn4zJJo4FHfeNFXnabZzOWrqO2TboYXKIfuht0x9+zFz1lwsECQQDnTYFIcgpsNW1kfGcgraP1LC3SpAfqamq07f91mvFpSoaZpBZ1Ghxkz5Z+4h+GmhLFdk0mHAD+IlEwPgOKfmD1AkEAuhNW7OIqimQsfaOolfyc9K1III4OqPjPXnJEsbZceZ1fESJUExHHfyc5Ectli6eTP32CZZVvky9yQU6cuinQJBAMxaSGdmAdlaVpyZ4E8ZuiqI7q8UJr4vaLkTMEiKLNE2e7bQJtssx3s1gCP3yZyVERKOE1khEqt0TECP+06LJtuOVUiUtNMLkeh11/RkCQQCaRy44Wo/r8sY10RGjPutFOnUs2bIdkVxDfVeaEejNNLVNveN+JT/8OW3l9dwuZPc07SHOEZX5OaEhMGthyu" 
                    } 
                ], 
                "signature": { 
                    "signatureAlgorithmID": "sha256WithRSAEncryption", 
                    "data": "oal8xbnW9kQmx6oUtOkTMfyF7pXJtu1K3456WTVUkmFhyA0du1PcmPcl+faKZcZ4siUXVYJXw/1DS2yxYq8U9HPH3CmSJtdX0oyiVmayutCRNWJYWLUK8TmXgTcxBOCjGXoj23Me7vG9qLibFwYzihkEIRiTIQ3GvgYdFeYN3Ac=" 
                } 
            } 
        } 
    ] 
    }, 

          "businessId": "ZjUxODNmYTI3NDczOWYzNjRmZTI0NjBhMzdmMWYzYTM6OlQxZS94Y1l1TGhqdGl4bXpkeFl0VXc9PQ==", 
          "method": "biometric", 
          "appAction": "registration" 
    } 
            ] 
    } 
     
  

**Attributes**
 
.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**customerBizId** *string*

Unique Id generated by WebSocket server against the business entry. 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**token** *string*

Generates token once the newly registered found to be unique. 
The Avatar app generates a unique identifier in the format "123456@avatarmail.io" and associates it with Avatar Inc. 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**Facekey** 

Face key is generated after the registration of the user.

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">


**Localprofiles**

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**Person** *String*

Name of the person related to the business who is registered.

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**Version-number** *Integer*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**serialNumber** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">


**subjectId** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**inheritsFrom** 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**subjectPublicKey** 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**coseId** *Integer*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**keyValue** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**validity**

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**notBefore** *Integer*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**notAfter** *Integer*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**subjectConsentObtained** *Boolean*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**assignedTo** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**verificationData** *String* 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**extensions** 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**type** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**version** *Integer*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**content** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**type** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**version** *Integer*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**content** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**signature** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**signatureAlgorithmID** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**data** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**businessId** *String*

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**method** *String*

Live face of the person is taken verification and face key is generated. 

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**appAction** *String*

Type of action that is taken

.. raw:: html

    <hr style="border: 1px solid #ccc; margin: 20px 0;">

**Attributes**

+---------------------------+-------------------+-------------------------------------------------------------------------+
| Fields                    | Type              | Description                                                             |
+===========================+===================+=========================================================================+
| auths                     |                   |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| customerBizId             | String            | Unique Id generated by WebSocket server against the business entry      |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| Token                     | String            | Generates token once the newly registered found to be unique            |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| Facekey                   | String            | Face key is generated after the registration of the user                |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| Localprofiles             |                   |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| Person                    | String            | Face key is generated after the registration of the user                |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| Version-number            | Integer           |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| serialNumber              | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| subjectId                 | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| inheritsFrom              |                   |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| subjectPublicKey          |                   |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| coseId                    | Integer           |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| keyValue                  | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| validity                  |                   |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| notBefore                 | Integer           |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| notAfter                  | Integer           |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| subjectConsentObtained    | Boolean           |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| assignedTo                | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| verificationData          | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| extensions                |                   |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| type                      | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| version                   | Integer           |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| content                   | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| signature                 | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| signatureAlgorithmID      | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| data                      | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| businessId                | String            |                                                                         |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| method                    | String            | Live face of the person is taken verification and face key is generated |
+---------------------------+-------------------+-------------------------------------------------------------------------+
| appAction                 | String            | Type of action that is taken                                            |
+---------------------------+-------------------+-------------------------------------------------------------------------+




