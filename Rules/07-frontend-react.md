# React Development Rules

Follow the existing React architecture.

## Components

Prefer:

- small components
- reusable components
- clear props
- predictable state management

Avoid:

- giant components
- excessive prop drilling
- duplicated UI logic
- unnecessary global state

## State

Use the smallest appropriate state scope.

Prefer:

local state
→ context
→ existing state library

Do not introduce Redux/Zustand/etc. if the application does not need it.

## API Calls

Centralize API communication when the project already has an API layer.

Handle:

- loading
- success
- empty state
- error
- retry where appropriate

## Forms

Validate:

- required fields
- data types
- formats
- business constraints

Display useful validation errors.

## Security

Never trust frontend authorization.

The backend must enforce permissions.

Do not place secrets in React environment variables if they are intended to be private.

Remember:

Frontend environment variables are generally exposed to the browser bundle.

## Performance

Avoid unnecessary:

- renders
- API requests
- expensive computations
- large bundles

Use memoization only when there is a demonstrated need.

## Accessibility

Interactive components should support:

- keyboard navigation
- labels
- semantic HTML
- meaningful error messages
- appropriate ARIA where necessary