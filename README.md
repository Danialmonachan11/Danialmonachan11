% German Job Papi Style Layout
\documentclass[10pt,a4paper]{article}

% Page margins
\usepackage[left=1.5cm,right=1.5cm,top=1.5cm,bottom=1.5cm]{geometry}

% Font setup
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{lmodern}
\usepackage{helvet} % Sans serif font
\renewcommand{\familydefault}{\sfdefault}

% Colors
\usepackage{xcolor}
% Color picked from the "German Job Papi" image (approximate standard nice blue)
\definecolor{mainblue}{HTML}{0E5484} 
\definecolor{textgray}{HTML}{404040}
\definecolor{dategray}{HTML}{666666}

% Graphics
\usepackage{graphicx}

% Icons
\usepackage{fontawesome5}

% Layout tools
\usepackage{paracol}
\usepackage{enumitem}

% Hyperlinks
\usepackage[hidelinks]{hyperref}

% No paragraph indent
\setlength{\parindent}{0pt}
\setlength{\parskip}{0.5em}

% Column setup
% Left column (Experience) wider, Right column (Skills) narrower
\columnratio{0.65} 
\setlength{\columnsep}{1cm}

% ================= CUSTOM COMMANDS =================

% Section Heading: ALL CAPS, BLUE, Bold
\renewcommand{\section}[1]{%
    \vspace{1.5em}%
    {\footnotesize\bfseries\color{mainblue}\MakeUppercase{#1}}%
    \par\vspace{0.5em}%
}

% CV Entry: Company, Location --- Title
% Date on next line
\newcommand{\cventry}[4]{%
    \noindent
    {\bfseries #1} \textemdash \ \textit{#2} \\
    {\small\color{dategray} #3} \par
    \vspace{0.3em}
    {\small #4} \par
    \vspace{0.8em}
}

% Project Entry
\newcommand{\projectentry}[3]{%
    \noindent
    {\bfseries #1} \hfill {\small\color{dategray} #2} \par
    \vspace{0.3em}
    {\small #3} \par
    \vspace{0.8em}
}

% Skill Section
\newcommand{\skillgroup}[2]{%
    \noindent\textbf{#1} \par
    {\small #2} \par
    \vspace{0.8em}
}

\begin{document}

% ================= HEADER =================
\noindent
\begin{minipage}[c]{0.70\textwidth}
    {\fontsize{24}{28}\bfseries\sffamily Danial Monachan} \\[0.2em]
    {\LARGE\color{textgray} Machine Learning Engineer | Industrial AI} \\[1em]
    
    {\small\color{textgray}
    \begin{tabular}{@{}l l}
        \faPhone \ +49 1590 6769410 & \faMapMarker* \ Cottbus, Germany \\
        \faEnvelope \ \href{mailto:danialmonachan11@gmail.com}{danialmonachan11@gmail.com} & \faPassport \ Indian (Residence Permit) \\
        \faLinkedin \ \href{https://linkedin.com/in/danial-monachan-b09494142}{LinkedIn} & \faGithub \ \href{https://github.com/Danialmonachan11}{GitHub}
    \end{tabular}
    }
\end{minipage}%
\hfill
\begin{minipage}[c]{0.25\textwidth}
    \centering
    \includegraphics[width=3.5cm,keepaspectratio]{image.png}
\end{minipage}

\vspace{1.5em}

% ================= BODY (2 Columns) =================
\begin{paracol}{2}

% ----- LEFT COLUMN (Experience, Projects, Education) -----

\section{Profile}
Machine Learning Engineer with hands-on experience building and deploying AI systems for industrial engineering environments. I specialize in transforming complex image and sensor data into production-ready analytics tools used by process engineers to improve yield and decision-making. My work sits at the intersection of applied machine learning, data engineering, and user-facing tooling. I focus on bridging research and production by designing scalable ML pipelines, interactive analysis platforms, and agent-based AI workflows that are robust, interpretable, and adopted by real users.

\section{Experience}

\cventry{ASML, Berlin, Germany}{Machine Learning Engineer (Working Student)}{07/2023 -- Present}{%
    \begin{itemize}[left=0pt, label=\textbullet, nolistsep]
        \item \textbf{Project: Deviation Predictor (AI/ML)}: Developed and industrialized a wafer surface reconstruction model to predict process deviations using incomplete metrology data. Applied SVD-based completion and uncertainty quantification, validating predictions against ground-truth measurements. Enabled earlier defect risk assessment and supported data-driven yield improvement decisions.
        \item \textbf{Project: Interactive Analytics Platform (Tooling)}: Designed and built an interactive visualization platform for high-resolution interferometry data (1024x1024), replacing fragmented manual analysis workflows. Centralized data exploration and comparison across experiments, reducing analysis time by $\sim$40\%. Actively used by 20+ process engineers in daily production support.
        \item \textbf{Tech}: Python, NumPy, scikit-image, Pandas, Dash/Plotly, Parquet, Git.
    \end{itemize}
}

\cventry{Hexaware Technologies, Bangalore, India}{Data Integration Engineer}{01/2021 -- 09/2023}{%
    \begin{itemize}[left=0pt, label=\textbullet, nolistsep]
        \item Designed and delivered end-to-end ETL pipelines for enterprise-scale datasets, owning solutions from requirements through production deployment.
        \item Implemented automated data quality checks and monitoring, reducing manual validation effort and improving data reliability.
        \item Collaborated with cross-functional stakeholders to ensure data availability for downstream analytics and reporting.
        \item \textbf{Tech}: Python, T-SQL, Azure Data Factory, SSIS, Git.
    \end{itemize}
}

\cventry{Hexaware Technologies, Chennai, India}{Associate Software Engineer}{01/2020 -- 12/2020}{%
    \begin{itemize}[left=0pt, label=\textbullet, nolistsep]
        \item Developed backend services and REST APIs for an enterprise Employee Leave Management System serving 5,000+ users.
        \item Contributed to database design, API integration, and production support.
        \item \textbf{Tech}: Python, SQL Server, REST APIs.
    \end{itemize}
}

\newpage
\section{Projects}

\projectentry{LLM Workflow Orchestration Framework}{2024}{%
    Designed a modular agent-based AI framework to orchestrate complex LLM workflows, supporting sequential and parallel execution patterns. Integrated retrieval-augmented generation (RAG) using vector databases to enable context-aware reasoning across multiple agents. Built the system with scalability in mind using asynchronous execution, standardized configuration (YAML/JSON), and API-based integration. \\
    \textbf{Tech}: LangChain, Langflow, PyTorch, Transformers, Qdrant, ChromaDB, FastAPI, asyncio.
}

\section{Papers}

\projectentry{Mix-and-Match Pruning}{Under Review, 2025}{%
    Research work investigating structural pruning strategies for Vision Transformers to improve computational efficiency while preserving model accuracy. Focuses on modular pruning approaches applicable to real-world deployment constraints.
}

\section{Education}

\cventry{BTU Cottbus-Senftenberg, Germany}{M.Sc. Artificial Intelligence}{10/2023 -- Present}{%
    Student Representative -- Head of Finances, Faculty Student Council (FSR AI).
}

\cventry{Karunya Institute, India}{B.Tech Computer Science}{2016 -- 2020}{%
    Grade: 8.4/10 ($\approx$ German 1.9)
}

\switchcolumn
% ----- RIGHT COLUMN (Skills, Languages) -----

\section{Job Related Abilities}

\skillgroup{Agentic AI \& GenAI}{%
- Multi-agent orchestration \\
- RAG pipelines, LLM integration
}

\skillgroup{Machine Learning}{%
- Deep learning with PyTorch \\
- Classical ML, scikit-learn \\
- Computer Vision (OpenCV, scikit-image)
}

\skillgroup{Data \& ML Systems}{%
- Data pipelines \\
- Feature processing \\
- Vector DBs (Qdrant, ChromaDB)
}

\skillgroup{Software Engineering}{%
- Python backend, APIs (FastAPI) \\
- Async systems, Docker \\
- Git, CI/CD
}

\section{Languages}
\skillgroup{English}{Fluent (IELTS 7.5)}
\skillgroup{German}{A2 (improving)}
\skillgroup{Hindi}{Native}
\skillgroup{Malayalam}{Native}

\section{Certifications}
\skillgroup{Azure Fundamentals}{AZ-900 (2020)}
\skillgroup{Data Analytics}{Visualization (2019)}


\end{paracol}

\end{document}
