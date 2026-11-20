# Little Sunshine Play School Website

## Run locally
1. Install Node.js (LTS).
2. Extract this folder.
3. Open a terminal in this folder and run `npm install`.
4. Copy `.env.example` to `.env`.
5. Set your admin username/password and a long random SESSION_SECRET in `.env`.
6. Run `npm start`.
7. Visit http://localhost:3000 and admin at http://localhost:3000/admin.

## Admin features
- Edit tagline, school description, phone, address and admission announcement.
- Upload gallery photos (12 MB each; JPG/PNG/GIF/WebP).
- Add YouTube/Vimeo video links with titles and descriptions.
- Edit programs and facilities.
- Save draft or publish. Draft edits are not visible to the public until Publish is clicked.

## Deployment
This project needs a Node hosting service and persistent storage because photos and content are saved on disk. On Render, create a Web Service, use `npm install` as build command and `npm start` as start command. Add environment variables from `.env`. Attach a persistent disk mounted at the project path (or configure uploads/content to use the mounted disk). Without persistent storage, uploaded photos and edits may be lost when the service restarts/redeploys.

## Security
Change the initial admin password and SESSION_SECRET before public deployment. Do not commit `.env` to a public repository. The server checks credentials server-side and admin actions require a session.
