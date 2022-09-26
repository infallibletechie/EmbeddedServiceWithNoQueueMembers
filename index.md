<html>
  <style type='text/css'>
    .embeddedServiceHelpButton .helpButton .uiButton {
      background-color: #005290;
      font-family: "Arial", sans-serif;
    }

    .embeddedServiceHelpButton .helpButton .uiButton:focus {
      outline: 1px solid #005290;
    }
  </style>
  <script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
  <script type='text/javascript'>
    var initESW = function(gslbBaseURL) {
      embedded_svc.settings.displayHelpButton = true; //Or false
      embedded_svc.settings.language = ''; //For example, enter 'en' or 'en-US'
      embedded_svc.settings.prepopulatedPrechatFields = {
        FirstName: “John”,
        LastName: “Doe”,
        Email: “john.doe @salesforce.com”,
        Subject: “Hello”
      };
      embedded_svc.settings.enabledFeatures = ['LiveAgent'];
      embedded_svc.settings.entryFeature = 'LiveAgent';
      embedded_svc.init('https://infallibletechie9-dev-ed.my.salesforce.com', 'https://infallibletechie9-dev-ed.my.salesforce-sites.com/', gslbBaseURL, '00D5f000001yZYJ', 'Embedded_Service_with_Bot_and_No_Queue_Members', {
        baseLiveAgentContentURL: 'https://c.la4-c1-ia4.salesforceliveagent.com/content',
        deploymentId: '5725f000000UhI1',
        buttonId: '5735f000000Uhrl',
        baseLiveAgentURL: 'https://d.la4-c1-ia4.salesforceliveagent.com/chat',
        eswLiveAgentDevName: 'EmbeddedServiceLiveAgent_Parent04I5f000000PZzzEAG_1837a2b6da5',
        isOfflineSupportEnabled: false
      });
    };
    if (!window.embedded_svc) {
      var s = document.createElement('script');
      s.setAttribute('src', 'https://infallibletechie9-dev-ed.my.salesforce.com/embeddedservice/5.0/esw.min.js');
      s.onload = function() {
        initESW(null);
      };
      document.body.appendChild(s);
    } else {
      initESW('https://service.force.com');
    }
  </script>
</html>
