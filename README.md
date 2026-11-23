Masih Labs Technologies Limited
masih06_Student_Progress_Tracker.html
README for beginners: every step, one small step at a time
What you are building. A private website where your trainers log in, open a student, see
exactly where that student is in the curriculum, and log the next lesson. It is free, and no
bank card is needed.
How long it takes. About 45 to 60 minutes the first time. You do not need to know
programming. You only copy and paste four pieces of text.
What you need before you start:
•  A computer is much easier than a phone for this setup. (Trainers can use phones
afterwards.)
•  A Google account (Gmail). Firebase uses it.
•  An email address to make a free GitHub account.
•  These files on your computer: masih05_Firebase_Rules.rules and
masih06_Student_Progress_Tracker.html.
•  Internet connection.
The 9 parts: 1 Make the Firebase project. 2 Turn on logins. 3 Make the database. 4 Lock
the database with rules. 5 Copy your four values. 6 Paste them into the file. 7 Put the
website online. 8 Create your admin account. 9 Add curriculum, students and trainers.
Menu names have changed. Firebase no longer has a "Build" menu. On the left you now
see Product categories: Databases & Storage, Security, Hosting & Serverless and
others. This guide uses those new names. Website screens change wording now and
then, so if a button looks slightly different, look for the closest match to the name in bold.
Part 1: Make the Firebase project
1.  Open your browser and go to console.firebase.google.com. Sign in with your Google
account.
2.  Click Create a project (it may say Add project).
3.  Type a name, for example masih-student-tracker. Click Continue.
4.  If it asks about Google Analytics, switch it off and click Create project. Wait until it
says your project is ready, then click Continue.
You should see: your project name with a small Spark plan label next to it, and a
menu on the left with Project Overview, Settings and Product categories. Spark is the
free plan, so you are fine. Ignore the Gemini and AI suggestions in the middle of the
page.
Part 2: Turn on logins
1.  In the left menu click Security. It opens a short list.
Page 1
masih06_Student_Progress_Tracker README
Masih Labs Technologies Limited
2.  Click Authentication.
3.  Click Get started.
4.  Open the Sign-in method tab and click Email/Password.
5.  Switch the first toggle (Email/Password) to Enable. Leave "Email link" off. Click Save.
You should see: Email/Password listed as Enabled.
Part 3: Make the database
1.  In the left menu click Databases & Storage. It opens a short list.
2.  Click Firestore (it may say Firestore Database). Do not choose Realtime Database.
3.  Click Create database. If it asks for an edition or database ID, keep the standard
choices it suggests.
4.  Choose a location near you (a Europe location is closest to Uganda). You cannot
change this later. Click Next.
5.  Choose Start in production mode. Click Create. Wait a minute.
You should see: an empty database screen with tabs such as Data and Rules.
Part 4: Lock the database with the rules
This step is what keeps your students private. Do not skip it.
1.  Click the Rules tab. You will see a box with some code.
2.  Click inside the box. Press Ctrl + A (select all) then Delete. The box is now empty.
3.  On your computer, right-click masih05_Firebase_Rules.rules, choose Open with,
then Notepad.
4.  In Notepad press Ctrl + A then Ctrl + C (copy everything).
5.  Go back to Firebase, click in the empty box and press Ctrl + V (paste).
6.  Click Publish.
You should see: a message that the rules were published.
Part 5: Copy your four values
1.  In the left menu click Settings, then Project settings.
2.  Stay on the General tab and scroll down to Your apps. (Shortcut: the Add app button
on the Project Overview page does the same job.)
3.  Click the round web icon that looks like </>.
4.  Type a nickname, for example tracker. Do not tick "Firebase Hosting". Click Register
app.
You should see: a box of code containing firebaseConfig with about seven lines.
Page 2
masih06_Student_Progress_Tracker README
Masih Labs Technologies Limited
5.  Find these four lines and copy the text inside the quotes of each: apiKey,
authDomain, projectId, appId. A good way: open a new Notepad window and paste
them there so they are safe. Then click Continue to console.
You can always find these values again: Settings, Project settings, General, Your apps.
apiKey:     "AIzaSy...long text..."
authDomain: "masih-student-tracker.firebaseapp.com"
projectId:  "masih-student-tracker"
appId:      "1:123456789:web:abc123..."
Part 6: Paste the four values into the tracker file
1.  Make a copy of masih06_Student_Progress_Tracker.html and rename the copy to
exactly index.html. (If you cannot see the ending .html, open any folder, click View,
then tick File name extensions.) Keep the original as a safe backup.
2.  Right-click index.html, choose Open with, then Notepad. Do not use Word.
3.  Press Ctrl + F, type PASTE_API_KEY, press Enter. You will land on this line:
const FB={apiKey:'PASTE_API_KEY',authDomain:'PASTE_AUTH_DOMAIN',
 projectId:'PASTE_PROJECT_ID',appId:'PASTE_APP_ID'};
4.  Replace each PASTE_... word with your real value. Delete only the PASTE_ word, and
keep the quote marks, commas and brackets exactly as they are. It should end up like
this:
const FB={apiKey:'AIzaSy...',authDomain:'masih-student-tracker.firebaseapp.com',
 projectId:'masih-student-tracker',appId:'1:123456789:web:abc123'};
5.  Press Ctrl + S to save. Close Notepad.
You should see: nothing special. The name must stay index.html, not index.html.txt.
Part 7: Put the website online with GitHub
1.  Go to github.com and click Sign up. Make a free account. Confirm your email.
2.  Click the + at the top right, then New repository.
3.  Repository name: student-tracker (any name without spaces). Choose Public. Click
Create repository. Public is fine: your file holds no student data, and the rules protect
the database.
4.  On the new page click the link uploading an existing file (or Add file, then Upload
files).
5.  Drag index.html into the box. Wait for it to finish, then click Commit changes.
6.  Click the Settings tab of the repository. In the left menu click Pages.
7.  Under "Build and deployment", set Source to Deploy from a branch. Set Branch to
main and the folder to / (root). Click Save.
Page 3
masih06_Student_Progress_Tracker README
Masih Labs Technologies Limited
8.  Wait 1 to 3 minutes and refresh the page. A link appears at the top, like the one below.
Click it.
You should see: your Trainer login page.
https://YOUR-GITHUB-NAME.github.io/student-tracker/
If you see "Open the HTML file and paste your Firebase config", Part 6 was not saved or
uploaded correctly. Go back to Part 6, fix it, and upload index.html again (Add file, Upload
files; it replaces the old one).
Part 8: Create your admin account
Do this before you share the link with anyone. The very first account becomes the admin.
1.  On the Trainer login page type your email, a password of 6 or more characters, and
your name.
2.  Click Create account (not Sign in).
You should see: three tabs at the top: Students, Curricula, Team. You are the admin.
3.  Write your password down somewhere safe.
Part 9: Use it
Add a curriculum (any subject).
1.  Click Curricula, then + New curriculum.
2.  Type a name. In the big box type one lesson per line. Start a line with # for a module (a
group of lessons). Example:
# Module 1: Basics
Safety rules
Using the multimeter
# Module 2: Building
Soldering practice
First circuit
3.  Click Save curriculum. You can edit it later; progress already recorded is kept.
Add a student.
4.  Click Students. Type the name, choose the curriculum, and optionally choose a photo.
Click Add student.
5.  Tap the student to open the profile. The Train next box shows the next lesson.
Log a lesson.
6.  In Log a session choose the lesson, a rating from 1 to 5, and tick Lesson completed
only if the student mastered it. Add skills, struggles and notes for the next trainer.
Click Save session.
You should see: the lesson appears under History and the progress bar moves.
Page 4
masih06_Student_Progress_Tracker README
Masih Labs Technologies Limited
If a lesson is not ticked completed, it stays as the next lesson so the following trainer
repeats it.
Download reports. On the student profile click Download Word for a .doc file. Click
Download PDF, and in the print window set the destination to Save as PDF.
Add a trainer.
7.  Send the trainer your website link.
8.  They click Create account and see "Waiting for approval".
9.  You open Team and click Approve beside their name. They press Check again and
are in.
10.  When a trainer leaves, click Revoke access. Their old session notes stay with the
students.
If something goes wrong
I cannot find "Build" in Firebase.
It was renamed. Use Security for Authentication, and Databases & Storage for
Firestore (see the note on page 1).
The page shows "Open the HTML file and paste your Firebase config".
Part 6 values are missing or the old file is online. Fix and upload index.html again.
"Permission denied" when saving.
The rules are not published (Part 4), or your account is not approved yet (Team tab).
Cannot create an account.
Email/Password is not enabled (Part 2), or the password is under 6 characters.
GitHub link shows "404".
Wait 3 more minutes. Check the file is named exactly index.html and Pages is set to
main and root.
Message about an unauthorised domain.
In Firebase open Security, Authentication, Settings, Authorized domains, click Add
domain and type YOUR-GITHUB-NAME.github.io.
Photo missing in the Word file.
Some Word versions hide it. Use the PDF.
Forgot a password.
In Firebase open Security, Authentication, Users, and look for the reset-password
option in that person's menu.
Good habits
•  Keep your admin password and your Google login private. Anyone with the Firebase
login can see all data.
•  Open the Team tab and press Download full backup once a month. Keep the file safe.
Page 5
masih06_Student_Progress_Tracker README
Masih Labs Technologies Limited
•  The free plan has daily limits, which are plenty for a small centre. Check Firebase pricing
if you grow to many hundreds of students.
•  To update the tracker later, edit the file again and upload index.html the same way.
Small dictionary
Firebase: Google's free service that stores your data and checks logins.
Firestore: The database inside Firebase.
Rules: The lock on the database that decides who may read or write.
GitHub Pages: Free hosting that turns your file into a website link.
Repository: A folder on GitHub that holds your files.
Admin: You. The person who approves trainers and can delete things.
Page 6
masih06_Student_Progress_Tracker README
