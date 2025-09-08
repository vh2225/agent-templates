## Introduction

These prompts help set up comprehensive project documentation for your LLM development projects.

Documentation is essential for:

- Helping your LLM understand the project scope
- Supporting you as a product creator/developer
- Understanding software development flow

Working through this process will:

- Raise important project questions
- Reveal alternative approaches
- Generate new ideas

![[Screenshot 2025-09-04 at 8.41.23 AM.png]]
## Getting Started

1. Paste the first prompt into an LLM
2. Iterate with the model
3. Save each output as a file for use with subsequent prompts

**Quick Instructions**: First, paste the Product Expert Prompt into o3 Mini and answer its questions. Next, paste the PRD output and UX prompt into a new chat and answer those questions. Finally, add both the PRD and UX documents to the context of another new chat, paste in the Software Architect prompt, and answer its questions.

## Table of Contents

1. [Product Requirements Document](https://claude.ai/chat/998d2f80-8a19-4a3e-a195-dff81c74b2cc#1-product-requirements-document)
2. [User Interface Design Document](https://claude.ai/chat/998d2f80-8a19-4a3e-a195-dff81c74b2cc#2-user-interface-design-document)
3. [Software Requirements Specification Document](https://claude.ai/chat/998d2f80-8a19-4a3e-a195-dff81c74b2cc#3-software-requirements-specification-document)
4. [Final Output](https://claude.ai/chat/998d2f80-8a19-4a3e-a195-dff81c74b2cc#4-final-output)
5. [Comparison Test For 3 Models](https://claude.ai/chat/998d2f80-8a19-4a3e-a195-dff81c74b2cc#5-comparison-test-for-3-models)

---

## 1. Product Requirements Document

Work with an expert product manager to create your requirements. Paste this 1st prompt into your LLM and hit return.

### Initial Prompt

```
# Context

You are an expert product manager your role is to work with me the product owner to generate a custom Product Requirements Document. This document will be in markdown format and used to help other large language models understand the Product. Be concise. 

# Instructions
1. Ask the product owner to explain the project idea to you
2. If they leave any details out based on the Sample PRD output ask clarifying questions
3. Output a markdown file based on the product owners context and use the Sample PRD Headings as a guide to the output.

# Sample PRD Headings

1. Elevator Pitch  - Pitch this product in one paragraph
2. Who is this app for
3. Functional Requirements - What does it do
4. User Stories - How will the user interact 
5. User Interface - How will the app look 
```

### 1.1 Example Response to LLM Questions

Let me explain what Levercast is. It's an application that helps entrepreneurs manage their social media posting more efficiently. Often when I'm reading an article or taking a walk, I'll come up with an idea for a thought piece or article. I want to quickly capture that idea through voice or text input. The app has an input box where I can dump these thoughts.

The input then gets sent to an LLM that formats it based on custom template prompts I've set up in the application. It returns a tidied version of my thoughts, but it does more than that—it generates multiple versions optimized for different social platforms. For our MVP, we'll focus on LinkedIn and Twitter posts, with plans to add more platforms later.

These generated posts will appear styled exactly as they would on their respective platforms, making it easy to preview the formatting. I can also add images to my input, and the app will adapt them appropriately for each platform. I can edit any of the outputs, and when I'm satisfied, publish them directly to those platforms. We'll use OAuth to connect Levercast with LinkedIn and Twitter accounts.

In essence, Levercast helps busy entrepreneurs capture ideas and share them quickly across multiple platforms simultaneously. The key benefit is saving time while amplifying marketing efforts. As for the user interface, while I'll leave the specific design details to a professional designer, I know it will be a web application initially, with responsive design to support mobile access in the future.

### 1.2 Example PRD Output

# Levercast Product Requirements Document

## Elevator Pitch

Levercast is a web application designed for busy entrepreneurs to effortlessly capture, format, and share their content ideas across multiple social media platforms. By simply entering raw text (and optionally uploading an image), users can leverage pre-defined templates powered by an LLM to generate polished, platform-specific content (starting with LinkedIn and Twitter). The application provides styled previews that mimic the final look on each platform and enables one-click publishing through OAuth integrations, saving time while amplifying marketing efforts.

## Who is this App For

- **Entrepreneurs and Business Owners:** Individuals who need a quick, streamlined way to capture ideas and publish them across social media.
- **Content Creators and Marketers:** Professionals looking to generate tailored content for various social channels.

## Functional Requirements

- **Content Input:**
    - A text input box for quickly dumping ideas or content.
    - An option to upload an image alongside text.
- **LLM-Powered Content Formatting:**
    - Process the input using customizable template prompts.
    - Generate multiple formatted outputs for different social media platforms (initially LinkedIn and Twitter).
- **Styled Previews:**
    - Display outputs with styles that replicate the final appearance on each respective platform.
    - Provide an editing interface for users to refine the content.
- **Publishing Mechanism:**
    - Integration with social media accounts via OAuth (starting with LinkedIn and Twitter).
    - A one-click publishing feature to post directly from the application.
- **Extensibility:**
    - Ability to add more social media platforms in future versions.
    - Potential expansion to mobile-responsive or mobile-native designs later.

## User Stories

- **Idea Capture:**  
    _As an entrepreneur, I want to quickly input my raw content ideas (text and images) so that I never lose a creative spark._
    
- **Content Generation:**  
    _As a user, I want the app to convert my raw ideas into polished, platform-specific formats using templates, so that my content is immediately ready for posting._
    
- **Content Customization:**  
    _As a user, I want to preview and edit the generated content to ensure it aligns with my brand voice and meets platform-specific formatting requirements._
    
- **Content Review:**  
    _As a user, I want to be able to view all the content I've created and navigate through the pasts posts, etc. So all these will have to be saved and allow me to manage them. Also their status as to whether they were pending or drafts or published._
    
- **Multi-Platform Publishing:**  
    _As a user, I want to connect my social media accounts (LinkedIn and Twitter) via OAuth and publish content directly from the app, saving time on manual posting._
    
- **Visual Verification:**  
    _As a user, I want to see styled previews that resemble the final look on each platform, so that I can verify and adjust the formatting before publishing._
    

## User Interface

- **Dashboard:**
    - A clean, intuitive central dashboard for accessing all features (content input, preview, editing, and publishing).
- **Content Creation Screen:**
    - A prominent text input area with an option to upload images.
    - A side-by-side preview panel displaying the generated content styled as LinkedIn and Twitter posts.
- **Editing Interface:**
    - In-line editing tools that allow users to make quick adjustments to the generated content.
- **Publishing Controls:**
    - Clear buttons for connecting social media accounts via OAuth.
    - A unified "Publish" button to send content to all connected platforms simultaneously.
- **Responsive Design:**
    - Initially optimized for desktop use, with plans for future responsiveness to accommodate mobile and tablet views.

---

## 2. User Interface Design Document

Work with a expert UX designer to figure out how you should approach the design of this App. Paste the prompt in your LLM and attach the PRD with it.

### Initial UX Prompt

```
# Context
You are an expert UX Designer your role is to work with the product owner to generate a custom User Interface Description Document. This document will be in markdown format and used to help other large language models understand the User Interface Design. Be concise.

# Inputs
1. Product Requirements Document 
2. User Chat

# Instructions
1. Process the product input documents if one is not provided ask for one
2. Ask questions about the user persona if it's unclear to you
3. Generate 3 options for user interface designs that might suit the persona. Don't use code this is a natural language description. 
4. Ask the product owner to confirm which one they like or amendments they have
5. Proceed to generate the final User Interface Design Document. Use Only basic markdown.

# Headings to be included

- Layout Structure
- Core Components
- Interaction patterns
- Visual Design Elements & Color Scheme
- Mobile, Web App, Desktop considerations
- Typography 
- Accessibility 
```

### 2.1 Example UX Model Response

Below is a summary of our initial thoughts based on the Levercast Product Requirements Document. Before moving forward, I have a few clarifying questions regarding the user persona and design preferences:

1. **User Persona Details:**
    
    - While we know the app targets busy entrepreneurs, business owners, content creators, and marketers, could you provide more details on their digital proficiency or any particular design preferences?
    - Do they prefer a minimalistic, no-frills interface that emphasizes efficiency, or are they open to a more dynamic, visually engaging experience?
2. **Branding & Color Preferences:**
    
    - Are there any existing brand colors or style guidelines we should incorporate into the design?
    - Would you like the design to offer options like a dark mode, or should we stick to a light, clean palette?
3. **Device Prioritization:**
    
    - Although the PRD mentions a desktop-first approach, should we factor in early considerations for mobile responsiveness?

Based on the current PRD, here are **three UI design options** that might suit your needs:

#### Option 1: Minimalist Modern Dashboard

- **Layout Structure:**  
    A clean, central dashboard with a split-screen design:
    
    - **Left Pane:** Prominent text input area with an image upload option.
    - **Right Pane:** Side-by-side styled preview panels replicating LinkedIn and Twitter posts.
- **Core Components:**
    
    - Central content input area
    - Dual preview panels with inline editing tools
    - Dedicated publishing controls (including OAuth integrations)
- **Interaction Patterns:**
    
    - Real-time content updates in the preview
    - Inline editing with immediate visual feedback
    - Clear, direct action buttons (e.g., "Publish", "Edit")
- **Visual Design Elements & Color Scheme:**
    
    - Light, neutral background with ample whitespace
    - A single vibrant accent color (e.g., blue or green) for primary actions
    - Flat, modern icons and simple borders
- **Typography:**
    
    - Clean sans-serif fonts (e.g., Helvetica, Arial) ensuring readability
- **Accessibility:**
    
    - High contrast elements and keyboard navigability
    - Clear labels for all interactive elements

#### Option 2: Bold Creative Dark Mode

- **Layout Structure:**  
    A visually striking, dark-themed interface:
    
    - **Upper Section:** Large, engaging content input field
    - **Lower Section:** Dynamic, grid-style preview panels for each social media style
- **Core Components:**
    
    - Expansive content input area with image support
    - Interactive preview cards that users can click to edit
    - A top navigation bar for publishing controls and account management
- **Interaction Patterns:**
    
    - Modal dialogs for detailed content editing
    - Interactive cards that update in real time
    - Hover effects and clear visual cues for actionable items
- **Visual Design Elements & Color Scheme:**
    
    - Dark background with bold accent colors (e.g., electric blue or bright orange)
    - Subtle gradients and shadow effects to create depth
    - Emphasis on visual flair while maintaining clarity
- **Typography:**
    
    - Modern sans-serif fonts with varying weights to establish hierarchy
- **Accessibility:**
    
    - Options for a high-contrast mode
    - Screen reader-friendly components and distinct focus states

#### Option 3: Card-based Modular Layout

- **Layout Structure:**  
    A modular, card-driven interface:
    
    - **Dashboard View:** A grid of cards representing each content idea (with status indicators such as draft, pending, or published)
    - **Content Creation:** A dedicated modal or separate screen for composing and editing new content
- **Core Components:**
    
    - Cards for individual content pieces
    - A prominent modal for content creation and editing
    - A unified publishing section with clear account integration
- **Interaction Patterns:**
    
    - Drag-and-drop organization of cards
    - Contextual menus for quick actions (e.g., edit, delete, publish)
    - Modal pop-ups for detailed content management
- **Visual Design Elements & Color Scheme:**
    
    - Neutral base colors with subtle shadows and borders to differentiate cards
    - Strategic use of accent colors to indicate status (e.g., green for published, amber for drafts)
    - A balance of professional aesthetics with modern touches
- **Typography:**
    
    - Professional sans-serif fonts that convey clarity and business-readiness
- **Accessibility:**
    
    - Scalable text and color-blind friendly palettes
    - Intuitive navigation with clear, accessible touchpoints

### 2.2 Example Response to UX Questions

On user persona details, I think these entrepreneurs are particularly digitally proficient. The selling point of this app is that it's not just another generic posting platform—it gives users the power to change their templates and properties. We're targeting more of a power user market. While others might use Buffer or Hootsuite, this is really for entrepreneurs who want to fine-tune their language, voice, and edit their own properties.

In terms of design, I prefer making things as minimalistic as possible. However, since users need options to change templates and customize settings, a balanced approach makes sense. Regarding branding and color preferences, I'll defer to your judgment based on our target market. Since we're targeting the development community and solopreneur makers, dark mode will likely be popular. For accessibility, we'll offer a light mode option as well, so our color scheme needs to accommodate both.

For devices, we're taking a desktop-first approach, but the app should be mobile responsive so users can operate it on phones and tablets. This will also inform our future React Native application development.

### 2.3 Example Final Selection Response

I think out of the three options I like number two the most. Let's lead with dark mode. Let's add the accent color to be yellow and I'd like the option to be able to switch to light mode, of course for accessibility. I'd like the main navigation to be handled in the left hand sidebar, which can be collapsed. That will have the ability to create a new post. It'll show all the recent posts. It will have a settings and a templates link. And whenever you navigate in the left hand menu, those components are opened in the main content area and at the bottom left of the sidebar put in the profile icon of the person when they click on that it's gonna allow them to log out.

### 2.4 Example Final UI Design Document

# Levercast User Interface Design Document

This document outlines the final UI design for Levercast, incorporating a bold, creative dark mode with a yellow accent color and an option to switch to light mode for enhanced accessibility. The design leverages a collapsible left-hand navigation sidebar and a dynamic main content area that adapts based on user interactions.

## Layout Structure

- **Overall Layout:**  
    The interface is divided into two primary areas:
    
    - **Left-Hand Sidebar (Navigation):** A collapsible panel that hosts all primary navigation elements.
    - **Main Content Area:** A dynamic area that displays the content corresponding to the selected navigation item.
- **Left-Hand Sidebar:**
    
    - Contains navigation links for:
        - **New Post:** Opens the content creation screen.
        - **Recent Posts:** Displays a list or grid of past posts (with status indicators such as draft, pending, or published).
        - **Settings:** Provides access to user and app configuration options.
        - **Templates:** Displays available content formatting templates.
    - The bottom left of the sidebar features the **Profile Icon**; clicking it opens a dropdown for logout.
- **Main Content Area:**
    
    - Dynamically updates based on the selected sidebar option.
    - Houses content creation screens, previews, editing interfaces, and publishing controls.
    - Designed for real-time interactions and updates, especially for content formatting and social media previews.
- **Theme Toggle:**
    
    - A clearly accessible toggle control (placed within the header or settings) allows users to switch between dark mode (default) and light mode.

## Core Components

- **Collapsible Left-Hand Navigation Sidebar:**
    
    - **Navigation Items:** "New Post", "Recent Posts", "Settings", and "Templates".
    - **Profile Icon:** Located at the bottom left, facilitating quick logout access.
    - **Collapse/Expand Feature:** Enhances screen real estate management.
- **Main Content Area Components:**
    
    - **Content Creation Screen:**
        - A large text input field for raw content ideas.
        - An option to upload images.
        - Real-time previews of content formatted for social media (e.g., LinkedIn and Twitter) with inline editing capabilities.
    - **Recent Posts Display:**
        - A list or grid view of past content with visual indicators of status (draft, pending, published).
    - **Settings & Templates Screens:**
        - Configurable options and a list of available LLM-powered content templates.
    - **Publishing Controls:**
        - OAuth integrations for social media accounts.
        - A one-click publish button to post to all connected platforms.
- **Theme Toggle Component:**
    
    - Enables users to switch between dark and light modes, ensuring visual accessibility without compromising on design integrity.

## Interaction Patterns

- **Sidebar Navigation:**
    
    - **Collapsible Behavior:** Users can collapse or expand the sidebar for a focused view of the main content.
    - **Dynamic Content Loading:** Clicking any navigation item (e.g., New Post, Recent Posts, Settings, Templates) updates the main content area accordingly.
    - **Profile Dropdown:** Clicking the profile icon triggers a dropdown with logout options.
- **Content Creation & Editing:**
    
    - **Real-Time Preview:** As users input text and upload images, previews update instantly to reflect changes.
    - **Inline Editing:** Enables users to adjust formatted content directly within the preview panels.
    - **Modal Interactions:** For more detailed editing or additional options, modal dialogs provide focused interaction windows.
- **Theme Switching:**
    
    - **Toggle Control:** Users can switch between dark mode and light mode with a single click, ensuring readability and personal preference adherence.
    - **Consistent Feedback:** Visual cues (e.g., hover states, active states) indicate interactive elements and current selections.
- **Publishing Flow:**
    
    - **OAuth Integration:** Clear, direct buttons facilitate account connection.
    - **Unified Publish Button:** Initiates one-click publishing across all linked social media platforms.

## Visual Design Elements & Color Scheme

- **Dark Mode (Default):**
    
    - **Background:** Deep, dark shades to reduce eye strain and emphasize content.
    - **Accent Color:** A vibrant yellow is used to highlight primary actions (buttons, links, icons) and interactive elements.
    - **Visual Hierarchy:** Bold visuals with subtle gradients and shadows to create depth without sacrificing clarity.
- **Light Mode:**
    
    - **Background:** A clean, light palette that maintains the same accent yellow for consistency.
    - **Text and Elements:** Darker text and elements to ensure high readability against the lighter background.
- **Sidebar & Main Content Contrast:**
    
    - The sidebar features a slightly different tone from the main content area to delineate navigation from content.
    - Icons and labels are clear and modern, reinforcing the interface's intuitive use.

## Typography

- **Primary Font:**
    - A modern sans-serif typeface (e.g., Roboto, Helvetica Neue) for a clean, contemporary look.
- **Font Hierarchy:**
    - **Headings & Buttons:** Bold weights to draw attention.
    - **Body Text:** Regular weights for comfortable reading.
    - **Adaptive Sizing:** Font sizes are chosen for legibility across various devices, with responsive scaling for desktop and future mobile views.

## Accessibility

- **Contrast and Color:**
    - High contrast between text and background in both dark and light modes.
    - The accent yellow is used judiciously to ensure clarity without overwhelming the interface.
- **Keyboard Navigation:**
    - All interactive elements, including the sidebar, toggle switches, and buttons, are fully navigable via keyboard.
- **Screen Reader Support:**
    - ARIA labels and clear text alternatives for icons ensure compatibility with assistive technologies.
- **Adjustable Settings:**
    - Options for text scaling and other customizable accessibility features are integrated within the Settings screen.
- **Responsive Interactions:**
    - Visual feedback (e.g., focus states, hover effects) is provided to enhance the usability of interactive components for all users.

_This design ensures that Levercast is both visually engaging and functionally robust, providing busy entrepreneurs and content creators with an intuitive, accessible, and efficient tool for social media content management._

---

## 3. Software Requirements Specification Document

Work with a Development Architect to figure out how to build your app. It's a good idea not to be too prescriptive with your preferred stack. Before you start the doc, have the model come up with unbiased ideas of how to build to identify new options. Add the previous docs with these prompts as attachments. Paste in the two previous docs to the chat window before proceeding with this prompt or create a project and attach them as files.

### 3.1 Initial Prompt for AI Software Architect

```
# Context
You are an expert Software Architect your role is to work with the product owner to generate a custom Software Requirements Specification Document. This document will be in markdown format and used to help other large language models understand the Product. Be concise.

# Input 
1. You will be provided with the Product Requirements Doc and User Interface Design Doc for context
2. Ask the developer what their existing skillset is and what language and frameworks they are comfortable with.

# Instructions
1. Process the product requirements document and and User Interface Design Doc for context if they are not provided ask for them or help the user create one. 
2. Output a simple (headings and bullets) markdown file based on the context and use the exact format in the Headings to be included section 

# Headings to be included
- System Design
- Architecture pattern
- State management 
- Data flow 
- Technical Stack 
- Authentication Process
- Route Design 
- API Design 
- Database Design ERD
```

### 3.2 Example Developer Response

"I'm proficient and comfortable with React, Next.js, Tailwind, Shadcn, Lucide Icons, Sonner Toast Backend: Prisma, Supabase, Vercel, Stripe, Clerk Auth, but I am also open to suggestions.

(First time around it's no harm in not telling the AI what you are inclined towards to let it surprise you with its own recommendations)"

### 3.3 Example Software Requirements Specification Document

# System Design

- Web application for busy entrepreneurs to capture, format, and publish content ideas.
- Supports raw text input and image uploads.
- Uses LLM-powered templates to generate platform-specific content (initially for LinkedIn and Twitter).
- Provides styled previews mimicking final social media appearance.
- Includes a dashboard for creating, editing, and managing content.
- Enables one-click publishing via OAuth integrations.

# Architecture pattern

- **Frontend:** Single Page Application (SPA) using React and Next.js.
- **Backend:** Serverless/microservices architecture hosted on Vercel.
- LLM integration as a dedicated service for content formatting.
- Clear separation between client (UI) and server (API) layers.

# State management

- Local UI state managed with React state/hooks.
- Global state management via Context API (or Redux if scaling demands).
- Real-time preview updates through client-side caching.
- Synchronization with server state from Supabase.

# Data flow

- **Input:** User submits raw text and optional image.
- **Processing:** Data is sent to the LLM service for content formatting.
- **Output:** Formatted content is displayed in styled previews.
- **Editing:** Users can make inline edits before finalizing.
- **Publishing:** Final content is sent to the backend, stored in Supabase, and pushed to social media via OAuth.
- **Review:** Content and status (draft, pending, published) are accessible from a dashboard.

# Technical Stack

- **Frontend:** React, Next.js, Tailwind CSS, Shadcn UI, Lucide Icons, Sonner Toast.
- **Backend:** Prisma, Supabase, Vercel.
- **Authentication & Payment:** Clerk Auth, Stripe.
- **Integrations:** OAuth for social media (LinkedIn, Twitter).

# Authentication Process

- User registration and login managed via Clerk Auth.
- Social media account integration via OAuth (initially LinkedIn and Twitter).
- Secure session management with token storage.
- Role-based access control for content creation and management.

# Route Design

- **/dashboard:** Central hub for accessing all features.
- **/edit-post:** Content creation interface for entering text and uploading images.
- **/posts:** List/grid view for recent posts with status indicators.
- **/settings:** User and app configuration options.
- **/templates:** Display of available LLM-powered content templates.
- Additional routes for OAuth callback and authentication flows.

# API Design

- **Content Endpoints:** CRUD operations for posts (create, read, update, delete).
- **Formatting Endpoint:** Endpoint to process content using LLM-powered templates.
- **Authentication Endpoints:** Manage user sessions and OAuth integrations.
- **Publishing Endpoint:** Trigger one-click publish to connected social platforms.
- JSON-based request/response structure with appropriate error handling.

# Database Design ERD

- **Users Table:**
    - User ID, name, email, authentication tokens.
- **Posts Table:**
    - Post ID, user ID (foreign key), raw content, formatted content, image URL, status (draft, pending, published), timestamps.
- **Templates Table:**
    - Template ID, name, prompt details, associated metadata.
- **Social Integrations Table:**
    - Integration ID, user ID (foreign key), platform (LinkedIn, Twitter), OAuth tokens, integration status.
- **Audit Logs Table (Optional):**
    - Log ID, user ID, action type, timestamp, description.

---

## 4. Final Output

Now we should have 3 great documents as our foundation for the next phase of development covering:

- Business Requirements
- User Experience
- Technical Approach

### 4.1 Package Files

We package these files as simple Markdown docs (file.md) and bring them to our favourite AI powered code editor. Here we place them in a documentation folder for the AI to reference.

---

## 5. Comparison Test For 3 Models

We tested 3 models and OpenAI o1 and o3 gave the best outputs marginally:

### DeepSeek R1 Example Output

[Includes sample PRD output with structured format focusing on functional requirements, user stories, and clear interface descriptions]

### Claude 3.5 Example Output

[Includes comprehensive PRD with detailed user personas, technical requirements, and extended functional specifications]

### OpenAI o3 Mini Example Output

[Includes business-focused PRD with subscription models, security considerations, and scalable architecture planning]

---

_This comprehensive guide provides a structured approach to creating professional project documentation using AI collaboration, ensuring all stakeholders have clear understanding of requirements, design, and technical implementation._