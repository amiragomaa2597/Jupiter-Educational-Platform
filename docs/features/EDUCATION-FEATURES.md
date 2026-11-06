# Education Features — Evidence Map

This document lists educational capabilities found in source. It is intentionally conservative.

## Student experience

| Capability | Frontend evidence | Backend evidence |
|------------|-------------------|------------------|
| Student hub | `features/people/student`, route `student` + `studentGuard` | Student APIs, enrollments `student-batches`, coins endpoints |
| My batches / courses | Student component uses batch/course/enrollment services | Batches, Courses, Enrollments controllers |
| Homework | `Homework/:courseId`, `Student-Homework/...` routes | `HomeworksController` |
| Materials | `materials/:course_id`, permission-aware | Course materials/session endpoints with permissions |
| Coins / ranking | `student-coins`, `jupiter-coins`, ranking routes | `CoinsLog`, student coins endpoints |
| Certificates | `Certificates` route / learning feature | `CertificatesController` |
| Attendance | Student attendance routes | `Attendances` / session attendance controllers |

## Staff / academic operations

| Capability | Frontend evidence | Backend evidence |
|------------|-------------------|------------------|
| Manage students | `view-students`, `students-view` + `app-data-view` | `StudentController` / `StudentV2Controller` |
| Manage courses | courses add/edit/details routes | `CoursesController` (+ V2) |
| Manage batches | batches add/edit/timetable | `BatchesController` / `BatchesV2Controller` |
| Enrollments | enrollment service | `EnrollmentsController` |
| Instructor dashboard | `instructor/:user_id` | `GetInstructorDashboard` |
| Admin dashboard | `admin/:user_id` | staff/user dashboard endpoints |

## Assessment

| Capability | Status | Evidence |
|------------|--------|----------|
| Quiz CRUD | Verified | `QuizController`, `QuestionsController`, EF `Quiz`/`Question`/`Answer`/`QuizGrade` |
| Realtime quiz session | Verified | `QuizHub`, `QuizRealtimeService`, hub map `quizhub` |
| Dedicated quiz-taking page in FE routing | **Needs confirmation** | No quiz route in `app-routing.module.ts` snapshot; notification/privacy references exist |

## Communications supporting education ops

- Notifications APIs + Angular SignalR notification hub client
- Email OTP password reset endpoints
- WhatsApp staff message tooling (authorized roles)

## Out of primary EdTech pitch (still real)

Finance, HR, competitions, agile project boards, software marketing site—verified modules, useful as breadth, but keep CV focus on educational core unless the employer asks.
