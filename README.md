# CTL-FinalProject
<b>The Author</b><br>
Kayla Gallagher, <a href="mailto:kgallagher6@su.suffolk.edu">kgallagher6@su.suffolk.edu</a>

<b>The Big Picture</b><br>
As the final class project for Coding the Law at Suffolk University Law School, we were tasked with creating a technical solution for a real-world legal problem. After thinking through the logistics and obvious hurdles of finding an external partner in the middle of a pandemic, my teammates, Joelle and Mike, and I chose to work with the Document Assembly Line Project and Suffolk LitLab. We produced three automated interviews for Mass Legal Services, the Boston Housing Authority and a General Release Form. 

Third party authorizations are common practice in the legal field to allow attorneys to acess the protected private information of their clients. These forms are often filled out during in-person consultations or meetings between the client and attorney. Due to the challenges of COVID-19 limiting safe access to in-person client meetings, these online interviews streamline the completion of these forms to be returned to the attorneys and agencies for use. 

<b><a href="https://github.com/kgallagher6/CTL-FinalProject/blob/main/CTL%20Project%20Pitch.pptx?raw=true">The Original Idea</a></b><br>
The users and stakeholders involved in this project are most clearly the client, their attorney and the agencies involved, as well as our external partner, the document assembly line project. Prior to the creation of these interviews, each of the forms could be downloaded, printed, filled out by hand, and returned to their respective attorney or agency. With COVID-19 bringing strict limitations to in person meetings these interviews allow for a user-friendly solution to completing these forms swiftly. These interviews will help the user, attorney or agency involved as they will have completed forms for use dispite the challanges brought by the pandemic, and improves accesability to those who may be unable to travel to such meetings.

As a group Joelle Ataya, Mike Carrol and I worked to complete three release forms requested by the Document Assembly Line Project. In our initial pitch, we only focused on two forms, the Attorney Authorization for Release from <a href="https://masslegalservices.org">Mass. Legal Services</a> in English and Spanish and the Authorization for Release from <a href="https://https://bostonhousing.org/en/Home.aspx">Boston Housing Authority</a>. Looking at the challenges that creating and translating an interview to a language that none of us were fluent in, we decided to pivot our initial MVP to be solely the english forms. At the request of our external partner, we added a third interview for a General Release Form. Since we now had three forms, each of us took point on one form. Kayla for the Mass. Legal Services Authorization, Mike for the BHA Authorization, and Joelle for the General Release form. 

<b>The Goal</b><br>
The goal of this project is to output three automated interviews that complete the release forms. Then, the client is instructed to download the form and either mail, e-mail, fax or deliver to their attorney or the BHA in accordance with the directions on the final page or the guidance of their counsel. 

I believe that the output of the project will ultimately make clients' lives easier by faciliating smooth communication between the user and the attorney or agency they are working with. It simplifies the completion of the forms and provides clear insturctions of how to reutrn them to the party they are working with.

Presently, our product is three different interviews that fill out an individual form. It is our intention to work on these forms in the future so that they could be integrated into a single interview where the output would trigger whichever form is needed based on how the questions are answered during the interview. 

<b>The Products</b><br>
The three interviews can be found<br>
  1.<a href="https://github.com/SuffolkLITLab/docassemble-AttorneyAuthorizationforRelease">Attorney Authoization for Release</a><br>
  2.<a href="https://github.com/SuffolkLITLab/docassemble-BHAReleaseAuthorization">Boston Housing Authority Release</a><br>
  3.<a href="https://github.com/SuffolkLitLab/docassemble-XXXXXXXXXXXXXXXXXXXXXXXXXX">General Release</a><br>

<b>The Good</b><br>
It works! You can view a quick demo <a href="https://github.com/kgallagher6/CTL-FinalProject/blob/main/Demo.mp4?raw=true">here</a>.

The interview itself allows for the attorney or agency to improve its efficiency. Rather than meeting with a client on an individual basis, taking time out of both of their days, an attorney can insturct as many clients as he or she needs to complete the interview and return the release forms to them. Thus, expanding their reach and output without disrupting their typical workflow. Additionally, it expands acess to clients who may not have the ability to take off work or meet with an attorney/agency. Expanding the reach on both the client end and the practictioner end.

<b>The Issues</b><br>
While this interview as it stands creates a desired output there are a few changes that I would like to implement in order to make for a more intiative user experience. I have found that there are a couple redundant or unnecessary questions based on user feedback:<br>
1. Asking "Did you start this case, or are you responding to a case that someone else started?"<br>
<i>Identifying the user as a plaintiff or defendant in this form is not necessary. The form only asks for the user and the opposing party, not what their role is in the dispute. This could be confusing to someone unfamiliar with the legal system. This further triggers plaintiff/defendant language in the question regarding the opposing party in this dispute. When this is resolved, we would like the language of the question to reflect what the form is asking</i>
2. Asking "Did anyone else file with you?"<br>
<i>This is a form for an individual and if anyone else is filing with them, they will likely have to fill this form out as well. When trying to remove this question we ran into performance issues that we are continuing to work on.</i>
3. The signature variables in the form itself, not the interview has logic that I'm not sure if it is even necessary to include, however the interview works, so this is something that can be revisited to clean up the variables in the future. Is it entirely possible that we only need users[n].signature in order to output the same result? I'm not positive, but the code as it is written was placed because I was told that it worked. Since it isn't currently broken, it is a lower priority item that will be tested and fixed eventually for a form that is uniform and easy to translate.
4. Ideally, this would call for more robust user testing as well. One place where I found that I fell short in testing the Attorney Authoization form was my bias towards beginning the form as a "plaintiff." Without realizing, nearly every interview we sampled, began as "starting a new case," which triggers the person filling out the form to be the plaintiff. Towards the end of the testing process this week, I discovered that when you begin the interview in the defendants shoes it throws an infinite loop error that we currently working to fix.

<b>The Feedback</b><br>
User Testing and Refinement.<br>

These interviews have gone through several rounds of testing and refinement. 

Each form was peer reviewed by each member of our group and feedback was given. We then posted the forms on the A2J slack and we received a veteran review where we took feedback both in public and private and modified our forms according to their suggestions. 

After the interviews were created, each interview was initially tested and run though multiple times by its point-person. Then, each partner tested the others' interviews for peer review. The feedback from these was reported in our weekly video meetup and refined for the next round of testing. 

When we ran into trouble with some code that we couldn't work out between the three of us, we turned both the the #coding-questions channel and our classmates to help with review and debugging. Once we discovered and fixed our problems, we refined again. These refined interviews were brought to demo in the beginning of December where we heard feedback from our partner, the Document Assembly Line, and have continued to interate on and refine our interviews based on the feedback that we have heard. 

This past week, the interviews were tested on an external user that fit a different demographical profile who might have a greater struggle using technology. The feedback from these users was given orally and their notes were taken into account for the current version of the interviews.

<b>Test User Alpha - a 35 year old male being represented by an individual in a dispute against an individual with a witness. Filling out and signing the form on a mobile device and then emailing it to themselves to download.<br></b>
<i>User Alpha found the interview easy to use, but commented that the signature lines at the bottom of the printable form didn't seem as necessary in a digital situation as they would be in its original form when someone is signing on the line, filling out the date and printing their name. User alpha also had questions about sending the form to the witness to sign rather than passing his mobile device to another person.
It is a possibility to remove these lines in the future for the form to appear more aesthetically efficient. During a pandemic, I see the concerns of sharing your mobile device but I also see the possible issues being able to send a witness the ability to sign, because there is no way to guarantee that they actually witnessed the form. This form does not have any notarization and the form was previously authored. Currently, it has not been confirmed whether a witness is necessary for the form to be valid. Feedback and consensus from Subject Matter Experts was that it depends on the practioner you are working with and the information that they are attempting to obtain. </i>

<b>Test User Bravo - a 60 year old woman being represented along with another individual by a firm in a dispute with an individual. Filling out the form on a computer and printing it to mail to her attorney.</b><br>
<i>User Bravo was confused by the question asking "Did anyone else file with you." For her the answer is yes, but she asked why it needed to be included in the form if it is for consent of the client to release personal information. It is a current issue we are working out. At the moment, when the question is removed, it has caused problems elsewhere in the interview and we are working to rectify this for a better user experience.</i>

<b>Test User Charlie - a 21 year old female being represented by an individual in a dispute against an organization. filling out the form on a computer with a witness present, emailing herself a copy and forwarding it to counsel.<br></b>
<i>User Charlie was able to complete the form. She was confused by the ability to add multiple witnesses at the question prompt, but in the directions it stated that you only needed "a" witness. She was not sure why it was relevant to ask whether she was the plaintiff or the respondent in the case and we took that feedback into account that it is not essential to this form. However, the basic questions focus on court forms and require that you fill out either that you are the plaintiff or who the plaintiffs are and it fills in the appropriate other_parties variable. If there was a way to change this and make it more condusive to the form it is not something that we have worked out at this time, but we continue to look for solutions. </i>

<b>Test User Delta - a 92 house mouse being represented by a firm of triplet cartoon ducks in a dispute against an anthropomorphic dog, filling out the form on a mobile device with his witness, a hot-headed duck, printing out and delivering to counsel. <br></b>
<i>Test User Delta, an anomoly, didn't have any issues filling out the form. He is incredibly optimistic, and suprisingly tech savy! He feels like all the issues can be resolved with a couple days of hardwork and has the utmost faith that our project could be used by real clients in need in the future.</i>

<b>The Future</b><br>
These forms are created in partnership with the Document Assembly Line Project, the volunteers of the document assembly line project will be availble to maintain, improve and iterate on the forms as needed and if the Boston Housing Authority and Mass Legal Services choose to update their forms in the future. 

As the Masslegalservices provided both an Authorization for Attorney relase in english and Spansih (Autorizacion de Abagodo/a), We hope that in the future we could have the interview translated into spansih to expand its accessability. 

We hope that the future of this project will lead to the creation of a uniform code specifically for legal forms that do not involve the courts. Presently, we have adapted the current code to our interviews to reflect that they do not require court permissions. 

<b>The External Partner </b><br>
Document Assembly Line Project is a volunteer effort born out of Suffolk Law's Legal Innovation and Technology Lab and Massachusetts Access to Justice's COVID-19 Task Force in order to make court and legal forms accessible through the obstacles this pandemic has created. 

<b>The Internal Partners</b><br>
Kayla Gallagher, Joelle Ataya and Michael Carroll are Suffolk Univserity Law School students who partnered in their Coding the Law class to create three seperate release forms for client use. 

Since we created interviews for three forms, we divided the work so each one would be the point person on one form, Kayla working on the Authorization for Release of Information via Masslegalservices, Mike working on the Boston Housing Authroity (BHA) Release, and Joelle working on a General Release form. Working in a group was incredibly beneficial for feedback and testing throughout the project. 

<b>FWIW, Thank You!</b><br>
Special Thanks to my partners Joelle Ataya and Mike Carroll for endless feedback and constant user-testing. The guidance of Suffolk LitLab, Volunteers of the Document Assembly Line Project, our classmates in the Coding the Law Class, and Professor David Colrusso for their expertise and assistance through countless questions, testing iterations, demos and feedback.

<h2><a href="VIDEOLINK">TL;DR, Watch the Video Instead</a>


</ CodingTheLawFinal></h2>
