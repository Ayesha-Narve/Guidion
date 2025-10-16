🎓 Guidion — Connecting Institutes and Guest Lecturers

🌐 Project Overview
Guidion is a web-based platform that bridges the gap between educational institutes, guest lecturers, and students, making the process of hiring, scheduling, verifying, and rating guest lecturers seamless and transparent.
The platform enables institutes to post or search for expert lecturers, manage bookings, and collect authentic feedback from students.
Lecturers can upload verified certificates, manage their profiles, and build credibility through ratings and blockchain-backed validation.
Students can share feedback after attending sessions and earn reward points for their active participation, redeemable for instant or larger rewards.
Guidion simplifies an otherwise manual and unstructured process into a smart, digital ecosystem that promotes trust, transparency, and engagement in academic collaborations.

🎯 Objectives
Create a unified platform to connect institutes and guest lecturers.
Simplify the session hiring, scheduling, and feedback process.
Ensure verification and trust through document uploads and blockchain-based validation.
Encourage student engagement through a reward point system.
Maintain transparency via feedback, ratings, and transaction tracking.

⚙ Flow of the Platform (Stepwise Execution)

1️⃣ User Registration & Login
Users can sign up as:
              🏫 Institute
              🎓 Guest Lecturer
              👩‍🎓 Student
After signup, authentication is handled to ensure secure login access for all users.
Each user type lands on their specific dashboard after login.

2️⃣ Institute Flow
1. Login / Signup → Lands on the Institute Dashboard.
2. The institute can post a requirement for a guest lecture or search experts based on:
        Subject expertise
        Availability
        Ratings
        Experience
3. Institutes can also post publicly if they want to invite applications from lecturers who match their requirements.
4. Lecturers can view and apply to these institute posts by sending a request.
5. Once an institute finds the right lecturer, it can send a direct booking request.
6. The lecturer gets a notification or email about the request.
7. Booking Confirmation → Lecturer accepts/rejects the request.
        On acceptance, booking is confirmed and added to both schedules.
8. Conduct Session → Session occurs on a decided date/time (venue may be decided in person).
9. Collect Feedback after the session:
        Students submit feedback directly.
        Institutes can also leave a review for the lecturer.
10. Institutes can track all bookings and lecturer transactions.
11. Transaction and payment details can optionally be secured via blockchain to ensure transparency and prevent tampering.
12. Institutes can build credibility by showcasing timely payments and verified collaborations.
13. 

3️⃣ Guest Lecturer Flow

1. Login / Signup → Lands on the Lecturer Dashboard.
2. Build a detailed profile including:
         Name, subject specialization
         Qualifications and years of experience
         Availability and preferred locations
3. View institute posts and send requests directly if requirements match.
4. Accept or reject invitations from institutes.
5. Update availability regularly to manage sessions.
6. After conducting a session:
         Receive feedback directly from students and institutes.
         View average rating and reviews on the dashboard.
7. Upload certificates for verification — optionally validated using blockchain for authenticity (ensuring certificates can’t be modified).
8. After successful sessions, lecturers can receive verified certificates or acknowledgments from institutes, enhancing their professional profile.
9. Maintain connections with multiple institutes and build reputation through ratings and verified collaborations.


4️⃣ Student Flow

1. Login / Signup → Students log in through their institute and access the student dashboard.
2. View attended or upcoming guest sessions scheduled by their institute.
3. After attending a session, students fill a feedback form:
         Ratings and comments
         Feedback remains anonymous (student names are hashed for privacy)
4. Feedback is stored securely in the database and contributes to the lecturer’s rating.
5. After submitting each feedback form, students earn reward points.
         Points can be used for instant rewards or saved for bigger prizes.
6. This reward system promotes genuine and active participation in feedback collection.



🧱 Database Schema (Modules)

🏫 Institute Collection:

instituteId
name
email
password
contactNumber
address
bookings: [bookingIds]
feedback: [feedbackIds]


🎓 Guest Lecturer Collection
lecturerId
name
email
password
subjects
qualifications
experienceYears
availability: { days, times }
certificates: [filePaths]
verified: Boolean
ratings: [values]
averageRating
linkedInstitutes: [instituteIds]

👩‍🎓 Student Collection
studentId
name
email
instituteId
feedbackGiven: [sessionIds]
rewardPoints: Number

📅 Booking Collection
bookingId
instituteId
lecturerId
sessionDate
status (pending / accepted / completed)


⭐ Feedback Collection
feedbackId
studentId (hashed/anonymized)
lecturerId
sessionId
rating
comments
date

🎁 Reward Collection
rewardId
rewardName
pointsRequired
rewardType (instant / collectible)

🧰 Tech Stack

Blockchain Layer	Technology- Contracts to be written in javascript (npx hardhat)

Frontend:          	EJS, HTML, CSS, JavaScript
Backend:          	Node.js + Express.js
Database:         	MongoDB + Mongoose
Authentication:	    JOI
File Uploads:     	Multer (for certificate uploads)
Blockchain:        	For certificate validation & transaction tracking
Version Control:   	Git & GitHub
Deployment:       	Render / Railway (Backend), Vercel / Netlify (Frontend)



💡 Key Features

Role-based login: Institute, Guest Lecturer, and Student.
Smart session booking and scheduling system.
Secure authentication and authorization with JWT.
Certificate upload and blockchain-based verification.
Feedback and rating system for quality improvement.
Student reward system with redeemable points.


🔮 Future Enhancements

🔗 Integration with Google Meet / Zoom APIs for live sessions.
💬 Real-time chat between institutes and lecturers.
💸 Payment gateway integration (Razorpay / Stripe).
📱 Mobile app using React Native or Flutter.
🔔 Email/SMS notifications for bookings and rewards.
📊 Admin analytics dashboard for activity reports.
Transparent booking and transaction tracking.
Dashboard for each user role.

Optional payment gateway integration.
