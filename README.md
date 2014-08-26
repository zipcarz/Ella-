Ella-
=====
#import <FacebookSDK/FacebookSDK.h>
FBLoginView *loginView = [[FBLoginView alloc] init];
[self.view addSubview:loginView];
FBLoginView *loginView = [[FBLoginView alloc] init];
// Align the button in the center horizontally
loginView.frame = CGRectOffset(loginView.frame, (self.view.center.x - (loginView.frame.size.width / 2)), 5);
[self.view addSubview:loginView];
  - (BOOL)application:(UIApplication *)application
didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    // Override point for customization after application launch.
    [FBLoginView class];
    ...
    return YES;
}
      - (BOOL)application:(UIApplication *)application
            openURL:(NSURL *)url
  sourceApplication:(NSString *)sourceApplication
         annotation:(id)annotation {

        // Call FBAppCall's handleOpenURL:sourceApplication to handle Facebook app responses
        BOOL wasHandled = [FBAppCall handleOpenURL:url sourceApplication:sourceApplication];

        // You can add your app-specific url handling code here if needed

        return wasHandled;
    }
