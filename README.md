 #  Dev Stack

Dev Stack is a responsive React application that helps users explore modern web development technologies and create their own technology stack. Users can browse technology cards, add technologies to their personal stack, and remove them whenever they want.

## 🌐 Live Demo


[View Live Demo](https://........vercel.app/)

## Project Preview

![Dev Stack Builder desktop preview](./public/dev-stack-desktop.png)



## Key Features

### 1. Explore Technologies

Browse 12 technologies loaded from a local JSON file.
Each card displays an icon, badge, description, category,
difficulty level, and star rating.

The layout shows one column on mobile, two on tablet,
and three on desktop.

### 2. Build and Manage Your Stack

Add technologies to the Your Stack panel and see the
selected count update immediately.

Selected cards display a highlighted border and a disabled
“✓ Added to Stack” button. Duplicate selections are prevented.
Users can remove one technology or clear the entire stack.

### 3. Clear Feedback and Loading States

React-Toastify provides notifications for adding technologies,
duplicate attempts, removing an item, and clearing the stack.

A loading spinner appears in the cards area while JSON data
is being fetched, keeping the surrounding section visible.

## Technology Stack

| Technology     | Purpose                                     |
| -------------- | ------------------------------------------- |
| React          | Components and interactive UI               |
| TypeScript     | Types for data, props, and handlers         |
| Tailwind CSS   | Styling and responsive layouts              |
| DaisyUI        | UI utilities and loading indicator          |
| React Icons    | Rating stars, check marks, and remove icons |
| React-Toastify | Action notifications                        |
| Vite           | Development server and production build     |
| JSON           | Technology catalog data                     |
| Vercel         | Website hosting                             |

## Design Details

- Sticky navbar with a responsive mobile layout.
- Hero section with a gradient heading and primary action.
- Responsive technology grid and stack sidebar.
- Mobile footer with centered branding and social links.
- Shared orange → pink → violet brand gradient.

The gradient is defined once as `--brand-gradient` in
`src/index.css`. Branding, the hero highlight, and the
Explore Technologies button reuse this value.

## Project Structure

| Path                                 | Description                            |
| ------------------------------------ | -------------------------------------- |
| `public/technologies.json`           | Technology catalog                     |
| `public/favicon.png`                 | Website favicon                        |
| `public/dev-stack-desktop.png`       | Project screenshot used in this README |
| `src/assets/`                        | Project images                         |
| `src/components/Navbar.tsx`          | Responsive navigation                  |
| `src/components/Hero.tsx`            | Hero content and banner                |
| `src/components/Technologies.tsx`    | Selected stack state and handlers      |
| `src/components/TechnologyCards.tsx` | Reads fetched data and renders cards   |
| `src/components/TechnologyCard.tsx`  | Individual technology card             |
| `src/components/Footer.tsx`          | Responsive footer                      |
| `src/Types/TechnologiesType.ts`      | Technology data type                   |
| `src/App.tsx`                        | Main application composition           |
| `src/index.css`                      | Global styles and shared gradient      |

## Getting Started

Download or clone this repository, then open a terminal
inside the project folder.

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open the local URL printed in the terminal.

## Available Scripts

| Command           | Description                               |
| ----------------- | ----------------------------------------- |
| `npm run dev`     | Start the development server              |
| `npm run build`   | Check TypeScript and build for production |
| `npm run preview` | Preview the production build locally      |
| `npm run lint`    | Run ESLint checks                         |

## Current Scope

The technology catalog loads from a local JSON file.
Stack selections are stored in React state and reset
when the page is refreshed.

Sign In and Sign Up are UI elements; authentication
is not implemented.


1. **Explore Technologies**  
   Browse technology cards with names, icons, categories, descriptions, ratings, and difficulty levels.

2. **Build Your Own Stack**  
   Add technologies to your personal stack and remove individual technologies when needed.

3. **Responsive User Interface**  
   The application works across desktop, tablet, and mobile screen sizes.

4. **Toast Notifications**  
   Users receive notifications when they add, remove, or clear technologies.

5. **JSON-Based Data**  
   Technology information is loaded from a separate JSON file.

---

#  React Questions and Answers

## 1. What is JSX, and why is it used in React?

JSX is a syntax that allows us to write HTML-like code inside JavaScript. React uses JSX to describe what the user interface should look like.

## 2. What is the difference between props and state?

Props are data passed from a parent component to a child component. State is data managed inside a component that can change over time.

## 3. What does the `useState` hook do, and where did you use it in this project?

The `useState` hook stores and updates data in a React component. I used it to store the technology list, loading status, and selected technologies in the user's stack.

## 4. What does the `useEffect` hook do, and why did you need it to load the JSON data?

The `useEffect` hook runs code after a component renders. I used it to load the technology data from the JSON file when the application starts.

## 5. Why does every item in a `.map()` list need a unique `key` prop?

A unique `key` helps React identify each item in a list. It allows React to update the correct item efficiently when the list changes.

## 6. What is conditional rendering? Show one place you used it.

Conditional rendering means displaying different UI depending on a condition.
