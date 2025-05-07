:root {
    --primary-color: #4361ee;
    --primary-light: #4895ef;
    --secondary-color: #3f37c9;
    --accent-color: #f72585;
    --light-color: #f8f9fa;
    --dark-color: #212529;
    --gray-color: #6c757d;
    --light-gray: #e9ecef;
    --success-color: #4cc9f0;
    --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.12);
    --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
    --shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);
    --border-radius-sm: 4px;
    --border-radius-md: 8px;
    --border-radius-lg: 12px;
    --transition: all 0.3s ease;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    line-height: 1.6;
    color: var(--dark-color);
    background-color: #f5f7ff;
    overflow-x: hidden;
}

h1, h2, h3, h4 {
    font-weight: 600;
    line-height: 1.2;
}

a {
    text-decoration: none;
    color: inherit;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.5rem;
}

/* Header Styles */
header {
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: white;
    padding: 2.5rem 0;
    text-align: center;
    position: relative;
    overflow: hidden;
}

header::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
    transform: rotate(30deg);
    z-index: 1;
}

header .container {
    position: relative;
    z-index: 2;
}

header h1 {
    font-size: 2.5rem;
    margin-bottom: 0.75rem;
    letter-spacing: -0.5px;
}

header p {
    font-size: 1.1rem;
    opacity: 0.9;
    max-width: 600px;
    margin: 0 auto;
}

/* Navigation */
nav {
    background-color: white;
    box-shadow: var(--shadow-sm);
    position: sticky;
    top: 0;
    z-index: 100;
    border-top: 1px solid rgba(0,0,0,0.05);
    border-bottom: 1px solid rgba(0,0,0,0.05);
}

nav ul {
    display: flex;
    list-style: none;
    justify-content: center;
    flex-wrap: wrap;
}

nav li {
    margin: 0 0.5rem;
}

nav a {
    display: block;
    padding: 1rem 1.25rem;
    color: var(--gray-color);
    font-weight: 500;
    transition: var(--transition);
    position: relative;
}

nav a:hover {
    color: var(--primary-color);
}

nav a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 0;
    height: 3px;
    background-color: var(--primary-color);
    transition: var(--transition);
    border-radius: 3px 3px 0 0;
}

nav a:hover::after {
    width: 100%;
}

/* Main Content */
main {
    padding: 3rem 0;
}

/* Ad Containers */
.ad-container {
    margin: 2rem 0;
    background-color: white;
    padding: 1rem;
    border-radius: var(--border-radius-md);
    box-shadow: var(--shadow-sm);
    text-align: center;
    border: 1px solid rgba(0,0,0,0.05);
}

/* Converter Card */
.converter-card {
    background-color: white;
    border-radius: var(--border-radius-lg);
    box-shadow: var(--shadow-md);
    padding: 2.5rem;
    margin-bottom: 2rem;
    border: 1px solid rgba(0,0,0,0.05);
    transition: var(--transition);
}

.converter-card:hover {
    box-shadow: var(--shadow-lg);
    transform: translateY(-2px);
}

.converter-card h2 {
    margin-bottom: 1.75rem;
    color: var(--primary-color);
    text-align: center;
    font-size: 1.75rem;
}

/* File Drop Area */
.file-drop-area {
    border: 2px dashed var(--light-gray);
    border-radius: var(--border-radius-md);
    padding: 3rem 1rem;
    text-align: center;
    transition: var(--transition);
    cursor: pointer;
    margin-bottom: 1.75rem;
    background-color: rgba(67, 97, 238, 0.03);
    position: relative;
    overflow: hidden;
}

.file-drop-area:hover {
    border-color: var(--primary-light);
    background-color: rgba(67, 97, 238, 0.05);
}

.file-drop-area.highlight {
    border-color: var(--success-color);
    background-color: rgba(76, 201, 240, 0.05);
}

.file-msg {
    display: block;
    font-size: 1.1rem;
    color: var(--gray-color);
    margin-bottom: 1rem;
}

.file-drop-area .icon {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 1rem;
    opacity: 0.8;
}

.file-drop-area input[type="file"] {
    display: none;
}

/* Options Section */
.options-section, .results-section {
    animation: fadeIn 0.5s ease;
}

.options-section h3, .results-section h3 {
    margin-bottom: 1.5rem;
    color: var(--gray-color);
    text-align: center;
    font-size: 1.25rem;
    position: relative;
    padding-bottom: 0.5rem;
}

.options-section h3::after, .results-section h3::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
    background-color: var(--primary-light);
    border-radius: 3px;
}

/* Form Elements */
.form-group {
    margin-bottom: 1.75rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.75rem;
    font-weight: 500;
    color: var(--dark-color);
}

.form-group select, .form-group input[type="number"] {
    width: 100%;
    padding: 0.875rem 1rem;
    border: 1px solid var(--light-gray);
    border-radius: var(--border-radius-md);
    font-family: inherit;
    font-size: 1rem;
    transition: var(--transition);
    background-color: white;
    appearance: none;
    background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='currentColor' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3e%3cpolyline points='6 9 12 15 18 9'%3e%3c/polyline%3e%3c/svg%3e");
    background-repeat: no-repeat;
    background-position: right 1rem center;
    background-size: 1rem;
}

.form-group select:focus, .form-group input[type="number"]:focus {
    outline: none;
    border-color: var(--primary-light);
    box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.1);
}

.custom-resolution {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-top: 0.75rem;
}

.custom-resolution input {
    flex: 1;
}

/* Compression Preview */
.compression-preview {
    margin-top: 0.75rem;
    display: flex;
    align-items: center;
    gap: 1rem;
}

.compression-bar {
    flex: 1;
    height: 8px;
    background-color: var(--light-gray);
    border-radius: 4px;
    overflow: hidden;
}

.compression-fill {
    height: 100%;
    background: linear-gradient(to right, var(--success-color), var(--primary-color));
    transition: width 0.3s ease;
}

/* Buttons */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0.875rem 1.75rem;
    border: none;
    border-radius: var(--border-radius-md);
    font-family: inherit;
    font-size: 1rem;
    font-weight: 500;
    cursor: pointer;
    transition: var(--transition);
    width: 100%;
    margin-top: 1rem;
    gap: 0.5rem;
}

.btn-primary {
    background-color: var(--primary-color);
    color: white;
    box-shadow: 0 4px 6px rgba(67, 97, 238, 0.2);
}

.btn-primary:hover {
    background-color: var(--secondary-color);
    transform: translateY(-2px);
    box-shadow: 0 6px 8px rgba(67, 97, 238, 0.25);
}

.btn-primary:active {
    transform: translateY(0);
}

.btn-secondary {
    background-color: white;
    color: var(--primary-color);
    border: 1px solid var(--primary-light);
}

.btn-secondary:hover {
    background-color: rgba(67, 97, 238, 0.05);
    border-color: var(--primary-color);
}

.btn .icon {
    font-size: 1.25rem;
}

/* Progress Container */
.progress-container {
    margin: 2rem 0;
    display: none;
    animation: fadeIn 0.5s ease;
}

.progress-bar {
    height: 8px;
    background-color: var(--light-gray);
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 0.75rem;
    box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
}

.progress-bar div {
    height: 100%;
    width: 0%;
    background: linear-gradient(to right, var(--success-color), var(--primary-color));
    transition: width 0.3s ease;
    border-radius: 4px;
}

.progress-text {
    display: flex;
    justify-content: space-between;
    font-size: 0.875rem;
    color: var(--gray-color);
}

/* Results Section */
.results-section {
    display: none;
}

#resultsList {
    margin: 1.5rem 0;
}

.result-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 1.25rem;
    background-color: white;
    border-radius: var(--border-radius-md);
    margin-bottom: 0.75rem;
    box-shadow: var(--shadow-sm);
    border: 1px solid rgba(0,0,0,0.05);
    transition: var(--transition);
}

.result-item:hover {
    transform: translateX(4px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.result-info {
    flex: 1;
    overflow: hidden;
}

.result-info p {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.result-info .file-name {
    font-weight: 500;
    color: var(--dark-color);
    margin-bottom: 0.25rem;
}

.result-info .file-size {
    font-size: 0.875rem;
    color: var(--gray-color);
}

.result-actions a {
    color: var(--primary-color);
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 0.25rem;
    padding: 0.5rem 0.75rem;
    border-radius: var(--border-radius-sm);
    transition: var(--transition);
}

.result-actions a:hover {
    background-color: rgba(67, 97, 238, 0.1);
}

/* Features Section */
.features {
    margin: 4rem 0;
}

.features h2 {
    text-align: center;
    margin-bottom: 3rem;
    color: var(--primary-color);
    font-size: 2rem;
    position: relative;
}

.features h2::after {
    content: '';
    position: absolute;
    bottom: -0.75rem;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 4px;
    background-color: var(--primary-light);
    border-radius: 4px;
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.feature-card {
    background-color: white;
    border-radius: var(--border-radius-lg);
    box-shadow: var(--shadow-sm);
    padding: 2rem 1.5rem;
    text-align: center;
    transition: var(--transition);
    border: 1px solid rgba(0,0,0,0.05);
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
}

.feature-icon {
    width: 60px;
    height: 60px;
    margin: 0 auto 1.5rem;
    background-color: rgba(67, 97, 238, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.75rem;
    color: var(--primary-color);
}

.feature-card h3 {
    margin-bottom: 1rem;
    color: var(--dark-color);
    font-size: 1.25rem;
}

.feature-card p {
    color: var(--gray-color);
    font-size: 0.95rem;
    line-height: 1.6;
}

/* Footer */
footer {
    background-color: var(--dark-color);
    color: white;
    padding: 4rem 0 1.5rem;
    position: relative;
}

footer::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 10px;
    background: linear-gradient(to right, var(--primary-color), var(--accent-color));
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 3rem;
    margin-bottom: 3rem;
}

.footer-section {
    position: relative;
}

.footer-section h3 {
    margin-bottom: 1.5rem;
    color: white;
    font-size: 1.25rem;
    position: relative;
    padding-bottom: 0.75rem;
}

.footer-section h3::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 40px;
    height: 3px;
    background-color: var(--primary-light);
    border-radius: 3px;
}

.footer-section p {
    color: rgba(255,255,255,0.7);
    margin-bottom: 1.5rem;
    line-height: 1.7;
}

.footer-section ul {
    list-style: none;
}

.footer-section li {
    margin-bottom: 0.75rem;
}

.footer-section a {
    color: rgba(255,255,255,0.7);
    transition: var(--transition);
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.footer-section a:hover {
    color: white;
    transform: translateX(4px);
}

.footer-section a .icon {
    font-size: 0.9rem;
    opacity: 0.7;
}

.copyright {
    text-align: center;
    padding-top: 1.5rem;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    color: rgba(255,255,255,0.5);
    font-size: 0.875rem;
}

/* Animations */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

/* Responsive Styles */
@media (max-width: 992px) {
    .container {
        padding: 0 1.25rem;
    }
    
    header h1 {
        font-size: 2.25rem;
    }
    
    .converter-card {
        padding: 2rem;
    }
}

@media (max-width: 768px) {
    header {
        padding: 2rem 0;
    }
    
    header h1 {
        font-size: 2rem;
    }
    
    nav li {
        margin: 0 0.25rem;
    }
    
    nav a {
        padding: 0.875rem 1rem;
        font-size: 0.95rem;
    }
    
    .converter-card {
        padding: 1.75rem;
    }
    
    .file-drop-area {
        padding: 2.5rem 1rem;
    }
    
    .custom-resolution {
        flex-direction: column;
        gap: 0.75rem;
    }
    
    .custom-resolution input {
        width: 100%;
    }
    
    .feature-grid {
        gap: 1.5rem;
    }
}

@media (max-width: 576px) {
    header h1 {
        font-size: 1.75rem;
    }
    
    header p {
        font-size: 1rem;
    }
    
    .converter-card {
        padding: 1.5rem;
    }
    
    .converter-card h2 {
        font-size: 1.5rem;
    }
    
    .features h2 {
        font-size: 1.75rem;
        margin-bottom: 2rem;
    }
    
    .feature-card {
        padding: 1.5rem 1rem;
    }
    
    .footer-content {
        gap: 2rem;
    }
}

/* Utility Classes */
.text-center {
    text-align: center;
}

.mt-1 { margin-top: 0.5rem; }
.mt-2 { margin-top: 1rem; }
.mt-3 { margin-top: 1.5rem; }
.mt-4 { margin-top: 2rem; }

.mb-1 { margin-bottom: 0.5rem; }
.mb-2 { margin-bottom: 1rem; }
.mb-3 { margin-bottom: 1.5rem; }
.mb-4 { margin-bottom: 2rem; }

.pulse {
    animation: pulse 2s infinite;
}
