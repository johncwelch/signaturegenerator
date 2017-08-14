# signaturegenerator
Sanitized version of an app I created to build signatures for Apple Mail.

So here's the thing: programmatically creating signatures for Apple Mail is a pain in the keister. The sane way to do it, i.e. AppleScript hasn't worked since 10.4. That's a long time.

In addition, doing it manually in Apple Mail creates some garbage HTML and if you want precise placement or are fussy about line spacing, you're out of luck. 

So I wrote this to help with all that as much as possible. It allows for some fairly fussy HTML, image placement, etc. Please take the time to read the source, it has a lot of info there. Not as well commented as I'd normally do, but close. This doesn't set up the actual sig file, because mail is a jerk. 

BEFORE YOU RUN THIS, create a dummy sig in mail with the right name. You don't care about anything else.

QUIT MAIL

Then go into ~/Library/Mail/Vwhatever/MailData/Signatures/ and find the file you just created. Leave the header lines in the file alone. They look something like:

Content-Transfer-Encoding: 7bit
Content-Type: text/html;
	charset=us-ascii
Message-Id: <647A606C-8172-48A3-B2E5-6272B90DA1AD>
Mime-Version: 1.0 (Mac OS X Mail 9.0 \(3054\))

As far as Vwhatever, that's based on what OS you're running. V5 = 10.13, V4 = 10.12, V3 = 10.11, which are the only three versions this supports.

Okay, so you got the sig file you want open, and mail isn't running. Run the app, then paste the results into the sig file you have open below the header lines. save it, close it, AND LOCK THE FILE BEFORE YOU OPEN MAIL! This is important because Mail will randomly rewrite that file if it "doesn't like" what you put in.

I kind of hate Apple Mail, it's why I use Outlook:Mac. 

So is this actually better than manual? probably not, but if you want more control over your sig files, it works. The real issue is how Apple does sigs in the first place, but good luck getting that fixed. 
