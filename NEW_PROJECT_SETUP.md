# 🚀 Starting a New Project with Agent Templates

## Quick Start (2 Minutes)

### Option 1: Direct Clone Method
```bash
# 1. Create your new project
mkdir my-awesome-project
cd my-awesome-project

# 2. Clone the agent templates
git clone git@github.com:vh2225/agent-templates.git agents

# 3. Copy the quick start guide
cp agents/QUICK_START_GUIDE.md ./PROJECT_SETUP.md

# 4. Initialize your project with agents
cat > ACTIVE_AGENTS.md << EOF
# Active Agents for My Awesome Project

## Phase 1: BUILD (Weeks 1-4)
- Build Agent: Marcus (Active)
- Frontend Dev: Emma (Active)
- Backend Dev: Liam (Active)

## Phase 2: MEASURE (Weeks 5-6)
- QA Lead: Jordan (Scheduled)
- Security: Zara (Scheduled)

## Current Sprint: Sprint 1
## Status: Development
EOF

# 5. Start development
npm init -y
git init
echo "# My Awesome Project" > README.md
```

### Option 2: Template Copy Method
```bash
# 1. Download templates directly
curl -L https://github.com/vh2225/agent-templates/archive/main.zip -o templates.zip
unzip templates.zip
mv agent-templates-main my-project
cd my-project

# 2. Customize for your project
vim README.md  # Update with your project name
```

## 📋 Step-by-Step Project Setup

### Step 1: Determine Your Project Type
```yaml
# Ask yourself:
Project_Size: Small / Medium / Large?
Duration: How many months?
Team_Size: How many people?
Technology: Web / Mobile / AI / Other?
```

### Step 2: Select Your Agents

#### For Small Project (1-3 developers, 1-3 months)
```bash
# Minimum viable team
cat > my-project/AGENTS.md << EOF
# Small Project Team

## Active Agents
1. Build Agent (Marcus) - Full-stack development
2. QA Agent (Jordan) - Testing & quality
3. Deploy Agent (Chen) - DevOps & deployment

## Schedule
- Week 1-3: Development (Marcus leads)
- Week 4: Testing (Jordan leads)
- Week 5: Deployment (Chen leads)
EOF
```

#### For Medium Project (4-10 developers, 3-6 months)
```bash
# Balanced team structure
cat > my-project/AGENTS.md << EOF
# Medium Project Team

## Core Team
1. Product Manager (Sarah) - Requirements & priorities
2. Build Lead (Marcus) - Development coordination
3. Frontend Dev (Emma) - UI/UX implementation
4. Backend Dev (Liam) - API & database
5. QA Lead (Jordan) - Testing strategy
6. DevOps (Chen) - Infrastructure

## BMAD Phases
- BUILD: Weeks 1-8 (Marcus, Emma, Liam)
- MEASURE: Weeks 9-10 (Jordan)
- ANALYZE: Weeks 11-12 (Riley)
- DEPLOY: Weeks 13-14 (Chen)
EOF
```

#### For Large Project (10+ developers, 6+ months)
```bash
# Use full BMAD framework
cp agents/BMAD_FRAMEWORK.md my-project/
cp agents/AGENT_ORG_STRUCTURE.md my-project/
# Customize with your specific needs
```

### Step 3: Initialize Project Structure
```bash
# Create standard project structure
mkdir -p my-project/{src,tests,docs,configs,.github/workflows}

# Create initial files
cat > my-project/package.json << EOF
{
  "name": "my-project",
  "version": "1.0.0",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "test": "jest",
    "lint": "eslint ."
  }
}
EOF

# Setup git
cd my-project
git init
git add .
git commit -m "Initial project setup with BMAD agents"
```

### Step 4: Configure Agent Communication
```bash
# Create communication plan
cat > my-project/COMMUNICATION.md << EOF
# Communication Plan

## Daily Standup
- Time: 9:00 AM
- Format: What I did / What I'll do / Blockers
- Participants: All active agents

## Channels
- Slack: #my-project
- GitHub: github.com/yourorg/my-project
- Docs: Confluence/Notion

## Code Review Process
- All PRs need 1 approval
- Build Agent reviews architecture
- QA Agent reviews tests
EOF
```

### Step 5: Define First Sprint
```bash
cat > my-project/SPRINT_1.md << EOF
# Sprint 1 Goals (Week 1-2)

## Build Agent (Marcus)
- [ ] Setup project structure
- [ ] Create basic API endpoints
- [ ] Implement core business logic

## Frontend Agent (Emma)  
- [ ] Create component library
- [ ] Build main layouts
- [ ] Implement routing

## QA Agent (Jordan)
- [ ] Setup testing framework
- [ ] Write initial test cases
- [ ] Create CI/CD pipeline

## Success Criteria
- Working development environment
- Basic features implemented
- Tests passing
- CI/CD operational
EOF
```

## 🎯 Real Example: E-commerce Site

```bash
# 1. Create project
mkdir ecommerce-platform
cd ecommerce-platform

# 2. Get agent templates
git clone git@github.com:vh2225/agent-templates.git .agents

# 3. Setup agents for e-commerce
cat > AGENTS.md << EOF
# E-commerce Platform - Agent Assignments

## Core Team (6 members)
- **Product Manager**: Sarah - User stories, priorities
- **Build Lead**: Marcus - Architecture, code reviews  
- **Frontend**: Emma - React, checkout flow
- **Backend**: Liam - API, payment integration
- **QA**: Jordan - Testing, quality gates
- **DevOps**: Chen - AWS deployment

## Phase Plan (12 weeks)
### Weeks 1-6: BUILD
- Product catalog
- Shopping cart
- User authentication
- Payment integration

### Weeks 7-8: MEASURE  
- Load testing
- Security testing
- User acceptance testing

### Weeks 9-10: ANALYZE
- Performance optimization
- A/B testing setup
- Analytics integration

### Weeks 11-12: DEPLOY
- Production setup
- Monitoring
- Launch preparation
EOF

# 4. Initialize with Next.js
npx create-next-app@latest . --typescript --tailwind --app

# 5. Add agent workflow
cat > .github/CODEOWNERS << EOF
# Agent code ownership
*.tsx @emma-frontend
*.ts @liam-backend  
*.test.* @jordan-qa
.github/* @chen-devops
EOF

# 6. Start development
npm run dev
```

## 📊 Quick Decision Tree

```
How many developers do you have?
├── 1-3 developers
│   └── Use: QUICK_START_GUIDE.md
│       └── Agents: Build, QA, Deploy
│
├── 4-10 developers  
│   └── Use: BMAD_FRAMEWORK.md (simplified)
│       └── Agents: PM, Build Team, QA Team, DevOps
│
└── 10+ developers
    └── Use: Full BMAD + ORG_STRUCTURE
        └── All agent teams activated
```

## 🛠️ Technology-Specific Starters

### For Next.js/React Project
```bash
# Quick setup
npx create-next-app my-app --typescript
cd my-app
git clone git@github.com:vh2225/agent-templates.git .agents
cp .agents/QUICK_START_GUIDE.md ./SETUP.md

# Assign agents
echo "Frontend: Emma" >> AGENTS.md
echo "Backend: Liam" >> AGENTS.md
echo "QA: Jordan" >> AGENTS.md
```

### For Python/FastAPI Project
```bash
# Quick setup
mkdir my-api && cd my-api
python -m venv venv
source venv/bin/activate
pip install fastapi uvicorn

# Get agents
git clone git@github.com:vh2225/agent-templates.git .agents

# Assign Python specialists
echo "Backend: Liam (Python)" >> AGENTS.md
echo "Data: Riley (ML/Analytics)" >> AGENTS.md
echo "DevOps: Chen (Docker/K8s)" >> AGENTS.md
```

### For Mobile App (React Native)
```bash
# Quick setup
npx react-native init MyApp
cd MyApp
git clone git@github.com:vh2225/agent-templates.git .agents

# Mobile-specific agents
echo "Mobile: Emma (React Native)" >> AGENTS.md
echo "Backend: Liam (API)" >> AGENTS.md
echo "QA: Jordan (Mobile Testing)" >> AGENTS.md
```

## ✅ First Day Checklist

```markdown
## Day 1 Setup Checklist
- [ ] Clone agent templates
- [ ] Choose project size (Small/Medium/Large)
- [ ] Select active agents (3-5 for small, 6-10 for medium)
- [ ] Create project structure
- [ ] Setup git repository
- [ ] Configure development environment
- [ ] Create first sprint plan
- [ ] Schedule daily standup
- [ ] Make first commit
- [ ] Start coding!
```

## 🎉 You're Ready!

After following these steps, you'll have:
- ✅ Project structure created
- ✅ Agent roles assigned
- ✅ Communication plan set
- ✅ First sprint defined
- ✅ Development environment ready

**Time to first commit: ~15 minutes**
**Time to working prototype: 1-2 weeks**

## 💡 Pro Tips

1. **Start Small**: Begin with 3 agents, add more as needed
2. **Use Phases**: Don't activate all agents at once
3. **Document Early**: Have agents document as they build
4. **Review Often**: Daily standups keep everyone aligned
5. **Iterate**: Adjust agent roles based on project needs

## 🆘 Troubleshooting

**Q: How do I know which agents to use?**
A: Start with Build, QA, and Deploy. Add others as complexity grows.

**Q: Can I rename the agents?**
A: Yes! The names are templates - customize for your team.

**Q: What if I don't need all phases?**
A: Use only what you need. BMAD is flexible.

**Q: How do agents "communicate"?**
A: Through PRs, documentation, comments, and your chosen chat platform.

---
*Ready to start? Pick your project type above and begin!*