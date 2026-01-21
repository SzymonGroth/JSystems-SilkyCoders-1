## Frontend Development Guidelines

## Code Formatting
- Indentation: 2 spaces.
- Semi-colons: Always use.
- Quotes: Use single quotes for strings, double quotes for JSX attributes.
- Line Length: Maximum 100 characters.
- Use ESLint and Prettier for automatic formatting.

## React & JSX Style
- Use Functional Components with Hooks. Avoid Class Components.
- Use arrow functions for component definitions.
- Destructure props in the function signature.
- File naming: Use PascalCase for components (e.g., `UserCard.jsx`) and camelCase for other files (e.g., `apiUtils.js`).
- JSX: Always use self-closing tags for components without children.
- Prefer fragments `<>...</>` over unnecessary `<div>` wrappers.

## React Hooks
- Follow the Rules of Hooks (only call them at the top level, only call them from React functions).
- Use `useEffect` sparingly; prefer derived state and event handlers.
- Custom Hooks: Extract complex logic into custom hooks prefixed with `use`.

## State Management
- Use `useState` for local component state.
- Use `useContext` for global state that doesn't change frequently (e.g., theme, user auth).
- For complex state management, consider using libraries like `Zustand` or `Redux Toolkit` (if the project grows).

## Components Structure
- Organize components by feature or commonality.
- Each component should be in its own directory if it has associated styles or tests.
- Keep components small and focused on a single responsibility.

## Performance
- Use `React.memo()` for expensive-to-render components.
- Use `useMemo` and `useCallback` to memoize expensive computations or stable function references when passed to memoized components.
- Optimize images and use lazy loading for routes (`React.lazy`).

## CSS & Styling
- Use CSS Modules for component-specific styling to avoid global scope pollution.
- Name CSS files as `ComponentName.module.css`.
- Use a utility-first CSS framework like Tailwind CSS if permitted.

## Testing
- Use Vitest as the test runner.
- Use React Testing Library for component tests.
- Focus on testing behavior from the user's perspective rather than implementation details.
- Filename pattern: `ComponentName.test.jsx`.

## API Calls
- Use `fetch` or `axios` for data fetching.
- Centralize API calls in a dedicated service or `hooks` layer.
- Handle loading and error states explicitly.

## Agent Changelog
- Follow the rules defined in the root `agents.md` regarding the `changelog.md`.
