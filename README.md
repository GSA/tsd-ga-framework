# TSD Google Analytics Framework
This repository documents the GSA IT Technology Solutions Division's (TSD) Google Analytics Framework for all digital services.

Due to the ever evolving nature of digital services, this framework will be updated from time to time to incorporate the latest standards to better support the use of Google Analytics.


### Google Analytics First
All Digital Services that are developed or maintained by the TSD division will leverage Google Analytics from the beginning. This is a firm requirement and should be included in the requirements of all projects. This means that each project must understand how this framework affects them and make the appropriate preparations to ensure that once deployed, the digital service is integrated with Google Analytics.


### Account and Property Structure
As our division matures in it's usage of Google Analytics, we have noticed how quickly management of the Google Analytics accounts get out of hand. In order to better manage this, we provide the following rules based upon [guidance from Google](https://support.google.com/analytics/answer/1009618?hl=en):


1. All Internal to GSA/FAS Digital Services will use a consolidated "TSD" Google Analytics Account.
2. External Digital Services, unless otherwise directed, will be placed under the Google Analytics Account for the Business Line, or Integrator that sponsors the Digital Service. (For example: Common Acquisition Platform, Integrated Technology Service, Customer Accounts & Research).
3. Each Digital Service, should have a single "Property" or "Tracking Code" under that Account. 
4. Development and Test environments should use the same property and views should be constructed to segment the data.

![Image](/assets/ga-account-structure.png)

### Every Page and View Should be Tracked
Modern web applications blur the line between web pages and web applications. At a bare minimum, every "page" or unique URL must include the appropriate Google Analytics Tracking framework or code. This is an important concept as not adhering to this will cause "holes" in your analytics which could lead to poor business decisions.


### Google Analytics Frameworks
Google Analytics tracks webpages in a standard way. However, the TSD division supports multiple web development technologies like; AngularJS, struts II, Django, Drupal, and Coldfusion. Each technology serves content in a different way, which may not lend itself to the standard way that Google Analytics tracks. In order to help teams worry less about customizing their Google Analytics implementation to work for their application, the TSD division has standardized various Google Analytics 3rd party and open source frameworks that should be used.


#### Drupal
When leveraging Drupal for your digital service, you should be using the standard [Drupal Google Analytics Module](https://github.com/CardinalPath/gas).

#### AngularJS
AngularJS is a phenominal web application framework that obscures the lines between traditional websites and web-applications. Encapsulating everything into API requests, It can deliver an entire web application in a single web page. This provides phenomenal value to the users, but can create challenges when attempting to track what users are using.

To combat this, your application should use [Angulartics](http://luisfarzati.github.io/angulartics/) or [Angularytics](https://github.com/mgonto/angularytics).


#### All Others
The United States Digital Service (USDS) Digital Analytics Program (DAP) has standardized their implementation of Google Analytics using [Google Analytics on Steroids (GAS)](https://github.com/CardinalPath/gas). If the other frameworks do not apply, the GAS framework should be used.


### DAP Support
In support of the USDS DAP program, all TSD digital services should be implementing the [USDS DAP](http://www.digitalgov.gov/services/dap/) tracking code on all websites. This is an additional tracking code in support of the DAP program.

**NOTE: DAP does note replace  the TSD Division Google Analytics**




### Event Tracking
All digital services should be configured to track the following events using [Event Tracking](https://developers.google.com/analytics/devguides/collection/analyticsjs/events):


1. File Downloads
2. Form Submissions
3. Opening pop-up, modal, or other type of "sub" window.
















