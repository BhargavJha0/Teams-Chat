# Mentorship Connect - React Native Mobile App

A cross-platform mobile application I built using React Native that connects mentors and mentees in the maritime industry. The app facilitates structured mentorship through real-time communication, session scheduling, and progress tracking.

This is a personal project I developed to explore full-stack mobile development with React Native on the frontend and a Spring Boot backend.

---

## Features

### Authentication & Onboarding
- Email/password login with "Remember Me" functionality
- Multi-step signup with role selection (Mentor / Mentee / Both)
- OTP-based email verification
- Forgot password flow with OTP reset
- Real-time username and email availability checks during registration

### Mentor Discovery & Connection
- Browse, search, and filter available mentors by skills
- Sort mentors (A-Z / Z-A)
- Send, withdraw, accept, or decline mentoring requests
- Detailed mentor profiles with experience, education, bio, and skills

### Real-Time Chat
- Instant messaging powered by WebSocket (STOMP protocol)
- End-to-end AES-256 encryption for all messages
- Typing indicators and read receipts
- File sharing support - images, videos, and documents
- Unread message count badges and last message previews

### Schedule & Meetings
- Calendar with month view (event dots) and day view (24-hour timeline)
- Create meetings with date/time pickers and automatic conflict detection
- Quick-link integration for Google Meet, Microsoft Teams, and Zoom
- Select multiple participants from your accepted connections
- Join Meeting button and per-session meeting notes

### Meeting Notes
- Add, edit, and delete notes for each scheduled event
- Timestamped entries with inline editing

### Profile Management
- Multi-tab profile editor - Profile, Education, Experience
- Photo upload, skills and language tags, social media links
- Country / State / City cascading selectors
- Read-only profile view for viewing other users

### Navigation & UX
- Bottom tab navigation - Home, Chat, Contacts, Schedule
- Drawer menu with seamless role switching (no re-login needed)
- Role-based dashboards for Mentors and Mentees
- Pull-to-refresh, loading states, and empty states throughout the app

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | React Native 0.84 |
| Language | JavaScript / TypeScript |
| Navigation | React Navigation (Stack, Bottom Tabs, Drawer) |
| Real-time Messaging | STOMP.js over WebSocket |
| Encryption | AES-256 via react-native-aes-crypto |
| Local Storage | AsyncStorage |
| UI Components | React Native Vector Icons, Reanimated, Gesture Handler |
| Calendar | React Native Calendars |
| Media Handling | Image Picker, Document Picker, File Viewer |
| Location Data | country-state-city |

---

## Getting Started

### Prerequisites
- Node.js >= 22.11.0
- React Native CLI
- Android Studio (for Android) / Xcode (for iOS)

### Installation

```bash
# Clone the repo
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# Install dependencies
npm install

# Run on Android
npm run android

# Run on iOS
cd ios && pod install && cd ..
npm run ios
```

---

## Project Structure

```
+-- App.tsx                  # Root navigator setup
+-- screens/
�   +-- LoginScreen.js       # Login page
�   +-- SignupScreen.js      # Registration flow
�   +-- OtpScreen.js        # OTP verification
�   +-- ForgotPasswordScreen.js
�   +-- MainNavigator.js    # Bottom tabs + drawer layout
�   +-- MenteeHomeScreen.js # Mentee dashboard
�   +-- MentorHomeScreen.js # Mentor dashboard
�   +-- ChatScreen.js       # Chat list
�   +-- ChatConversationScreen.js  # 1-on-1 messaging
�   +-- ScheduleScreen.js   # Calendar views
�   +-- CreateScheduleScreen.js    # Create meetings
�   +-- ScheduleDetailScreen.js    # Event details
�   +-- MeetingNotesScreen.js      # Notes per meeting
�   +-- MyContactsScreen.js # Connected users
�   +-- SeeAllMentorsScreen.js     # Browse mentors
�   +-- EditProfileScreen.js       # Edit profile (tabs)
�   +-- UserProfileScreen.js       # View user profile
+-- android/                 # Android native code
+-- ios/                     # iOS native code
+-- package.json
```

---



## License

This project is for personal and educational use.
