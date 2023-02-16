# Referer Chain

Case 1: ```CRM user``` >refer> ```Normal User```

-> Need an Endpoint to get refferer_token

Case 2: ```CRM user``` >refer> ````Normal User```` >refer> ```Normal User```

-> Using the same endpoint in case1

Case 3: Join a Live stream from the referer link

-> refferer_token already there.

# ENV VARIABLE

  import { Environment } from './environment.type';
  import { gitHash } from './git.hash';

  export const environment: Environment = {
    gitHash,
    agora: {
      appId: '3dfef56db2fa4d9c840d2e709ddcd5ab',
    },
    allowedIframeDomains: ['shoppopup.tv'],
    auth0: {
      clientId: 'PsDnj6VvzdpVEPIQIpuomS54dkQZwNA8',
      domain: 'verbtech.auth0.com',
      providers: [
        'production-salesforce',
        'windowslive',
        'facebook',
        'twitter',
        'apple',
        'google-oauth2',
      ],
      redirectUrl: '/login/auth0',
    },
    coreEnvironment: {
      awsAccountId: '198337867994',
      awsIdentityPoolId: 'us-east-1:93fa015c-a836-4bdc-a9f9-4ba1bf71c8ed',
      awsRegion: 'us-east-1',
      bucketUrl: 'https://corejs-videos-processed.s3.amazonaws.com/qa',
    },
    envName: 'dev',
    events: {
      apiEvents: {
        enabled: true,
      },
      firebaseAnalytics: {
        enabled: true,
        apiKey: 'AIzaSyC8C7wUGCVSnCsmAwrheAB2Tp4a2sDK0PI',
        authDomain: 'verb-live-mobile.firebaseapp.com',
        databaseURL: 'https://verb-live-mobile.firebaseio.com',
        projectId: 'verb-live-mobile',
        storageBucket: 'verb-live-mobile.appspot.com',
        messagingSenderId: '928540542909',
        appId: '1:928540542909:web:a72d0405b80429d33f34d4',
        measurementId: 'G-QVTXB2PC06',
      },
      pendoAnalytics: {
        enabled: true,
      },
    },
    launchDarkly: {
      apiKey: '5f4f0eadaf7868097fcd9adf',
    },
    logging: {
      consoleEnabled: true,
      sentryDsn:
        'https://2c54c0afc6564b8c9fd9067ee8d9e805@o225848.ingest.sentry.io/5448159',
      sentryEnabled: false,
    },
    maximumAttendees: 250,
    production: false,
    pusher: {
      appKey: '57427123157cd3707c84',
      cluster: 'us2',
    },
    streamServer: {
      debug: false,
      domain: 'stream-staging.verb.tech',
      keepAlivePeriod: 15000,
      maxRetries: 5,
      port: '443',
      relayHostUrl: 'localhost',
      remoteMessagingServerUrl:
        'wss://3avej3fmfj.execute-api.us-east-1.amazonaws.com/staging',
    },
    stripe: {
      apiKey: 'pk_test_Ghcu052smb6jge7i83MwgeSm',
    },
    supportEmailAddress: 'support@verb.tech',
    timeLimitInMinutes: 60,
    translationBaseUrl: '',
    verbServices: {
      apiKey: 'test1234',
      apiUrl: 'http://localhost:3000/dev',
      authEndpoint: 'stream/authenticate',
      authHeader: 'x-auth-token',
      authUsePost: false,
      noAuthRedirectUrl: undefined,
      storeApiUrl: 'https://staging-api.verb.tech',
    },
    video: {
      height: 360,
      width: 640,
    },
  };
