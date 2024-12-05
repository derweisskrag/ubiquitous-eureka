# Assignment: Find issues on EasyMedAi website

## UI/UX

I cannot see my models, I have to search for them. Solution: Add them to NavBar: Dashboard and there specify new navbar. Why not? Each page can have unique navbar.

Reproduce: Create a model. Task find it? Solution: Click on the logo and watch recent Activity. It is a feed where you can see your recent activity.

I would like to simplify user life and add dashboard button to navigate to it, or add button "view models" for users.

After deleting: you can highlight: DANGER ZONE like GitHub and inform users: Destructive action. Colour it so that they see (red), and make them type some secret word to confirm action.

## Security

Allowed me to set 123456 as password. Questions security. It should NOT allow simple passwords.

Using MS Edge tool revealed:

> You use _session_id, and I couldnt see JWT tokens: refresh and access tokens? Not found. Assume: Session-based authorization. Let me see weak password, used to send confirm email (JWT follows same given nodemailer). 

### How to fix?

Given the 2-step-authorization, it is safe. However, validate the passwords and avoid allowing users to set weak passwords.

Why JWT? Would enable you to let users use both phone and laptop or PC to be logged in on all devices using JWT access tokens.

### Permission

Forbidden
You don't have permission to access this resource.

Apache/2.4.29 (Ubuntu) Server at easymed.ai Port 80

How to reproduce: Go to Models. Create. Edit to add random README.md. Then select link and paste into the browser. Enter credentials. Get the error.

Should: Unknown
Actual: Error 403 -> Not permitted. Meaning I got no permission, because according: "user:my-actions" doesn't include to be able to view my git? 

Upon following instructions: refresh and then everything is created. Nice! 

#### More Permissions

Reproduce: Go to the EasyMedAi, log in and create model, and check out other modelds. What permissions are there?

I can delete my model. I can edit. I can view. I can create more.

I can view other models. I cannot edit them. I cannot delete them. Fine!

Ok

## Performance

When you enter wrong credentials, it reloads. Not Reactive application. Reload page => Possible performance (Gotta test).

Performance: Slow because UI/UX is taking time:

Using MS Edge


Largest Contentful Paint (LCP): 0.27 s
Your local LCP value of 0.27 s is good.

Cumulative Layout Shift (CLS): 0
Your local CLS value of 0 is good.

Interaction to Next Paint (INP): 48 ms
Your local INP value of 48 ms is good.

INP interaction: pointer

#### Conclusion

Make UI/UX loader faster by making UI/UX simpler and more accessible: adding colours, updating form's style to let users (being blind or insensitive to certain colours) to type and use the form.
For optimization: you can use (not sure yet) the game development technique: Marshing Cube. You can render the page as much as user views/needs to. It happens on your web-page: when scrolling down, you 
render them.

### Not Accessible When you enter invalid credentials: shows the error message on the client side, but is not visisble to users. Field arent coloured to RED. Web-site doesnt benefit from using advanced CSS to :user-valid and :user-invalid.

I am checking the page: https://easymed.ai/auth/do_login (auth page)
Design: Mobile: Not good loking. Margins I guess. Checked via phone and MS Edge tool 
Tablet & Laptop & PC are same as Mobile. So, Consistent UI/UX but lacks Margin I guess. Design issue.

Found behavior: 405 Error not handled. 
