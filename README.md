Build a full-stack Child Nutrition & Meal Planning Web Application with the following complete specifications:
🔐 Authentication & Role-Based Access Control
Implement a multi-role authentication system with 4 distinct user types: Mother/Parent, Nutritionist, Pediatrician, and Admin. All sign-ups must go through Admin approval before access is granted. Each role has its own dashboard, permissions, and workflows.
👩 Role 1: Mother / Parent
Sign-Up Fields: Username, role selection, contact number, password.
Child Profile Setup (post sign-up):
Number of children
Each child's name, age, gender, location
Meal preferences (vegetarian, non-vegetarian, vegan, etc.)
Food allergies (multi-select + custom input)
Known health conditions
Meal Planning Dashboard:
Calendar view to select care dates and reset/regenerate meal plans
Auto-generate 5 meals per day per child: Breakfast, Mid-Morning Snack, Lunch, Afternoon Snack, Dinner
Each meal card must display:
Recipe name and step-by-step instructions
Full nutritional breakdown (calories, protein, carbs, fats, vitamins)
Alternative ingredient suggestions
Option to exclude specific ingredients
Ability to submit a request to a Nutritionist for a customized or medically-reviewed meal plan
Notification system to receive approved/modified meal plans from Nutritionist
🥗 Role 2: Nutritionist
Sign-Up Fields: Username, role, contact number, password, certification upload (PDF/image).
Nutritionist Dashboard:
View and manage incoming parent requests for meal plan modifications
Access each child's full profile: allergies, health conditions, meal preferences
Review auto-generated meal plans and make modifications
Add professional notes to each meal or recipe
Publish/approve the final meal plan back to the parent
Certification verification status shown on profile
👨‍⚕️ Role 3: Pediatrician
Sign-Up Fields: Username, role, contact number, password, medical license/certification upload.
Pediatrician Dashboard:
View children's health condition profiles linked to their accounts
Approve or flag pediatrician-specific requests raised by parents or nutritionists
Add or update medical notes on specific meals or nutritional plans
Flag allergens or contraindicated ingredients based on a child's condition
Coordinate with nutritionist for medically-safe meal planning
🛡️ Role 4: Admin
Admin Dashboard:
View all pending sign-up requests across all roles
Approve or reject accounts with reason
Verify uploaded certifications for Nutritionists and Pediatricians
Manage all accounts: view, edit, suspend, or delete
View and respond to user queries/support tickets
Monitor overall platform activity and system integrity logs
🍽️ Meal Planning Engine
Each child gets a personalized 5-meal/day plan based on their profile data
Recipes must be appropriate for the child's age group
Nutritional values must be calculated per serving and per child's daily requirement
System must flag if a generated recipe contains a known allergen
Calendar integration: parents can set active care date ranges; plans reset or regenerate based on calendar
Ingredient exclusion logic: if an ingredient is excluded, the system suggests a safe alternative
📋 Additional Features
Notification System: Role-based notifications (e.g., parent notified when plan is approved, admin notified on new sign-up)
Request Workflow: Parent → requests review → Nutritionist/Pediatrician reviews → approves/modifies → published back to parent
Certification Management: Upload, verify, and display certification status badges on professional profiles
Audit Trail: Log all changes to meal plans with timestamps and editor role
Responsive Design: Mobile-friendly UI for all dashboards
Search & Filter: Admins and professionals can search children/users by name, condition, or location
🛠️ Tech Stack Suggestion (optional, adjust as needed)
Frontend: React.js or Next.js with Tailwind CSS
Backend: Node.js with Express or Django REST Framework
Database: PostgreSQL or MongoDB
Auth: JWT-based authentication with role middleware
File Storage: AWS S3 or Cloudinary for certification uploads
Calendar: FullCalendar.js integration
