# Telugu News Adda - Django Blog Website

A comprehensive Django-based Telugu news website with advanced content management, image optimization, and responsive design features.

## 🌟 Features

### 📰 Content Management
- **Rich Text Editor**: CKEditor 5 integration with custom toolbar
- **Multi-language Support**: Telugu and English content
- **Category Management**: Hierarchical category structure
- **Post Gallery**: Multiple image galleries per post
- **YouTube Integration**: Embedded video support
- **SEO Optimization**: Meta tags, descriptions, and friendly URLs
- **Featured Posts**: Highlight important content
- **Draft System**: Save and publish posts later

### 🖼️ Image Management
- **Automatic WebP Conversion**: All images converted to WebP format
- **Image Compression**: Intelligent quality optimization
- **Responsive Images**: Automatic resizing for different screen sizes
- **Gallery Management**: Organized image galleries with captions
- **Unused Image Cleanup**: Management command to remove orphaned files
- **Custom Storage**: Optimized file storage with compression

### 🎨 User Interface
- **Responsive Design**: Mobile-first Bootstrap 5 implementation
- **Telugu Typography**: Custom Ramabhadra font integration
- **Modern UI**: Gradient backgrounds and smooth animations
- **Breaking News**: Scrolling news ticker
- **Category Colors**: Visual category identification
- **Hover Effects**: Interactive elements with smooth transitions

### 🔒 Security & Performance
- **Environment Variables**: Secure configuration management
- **Database Flexibility**: SQLite, PostgreSQL, MySQL support
- **Image Optimization**: Automatic compression and format conversion
- **Caching Ready**: Prepared for production caching
- **CSRF Protection**: Built-in security measures

## 🛠️ Technology Stack

- **Backend**: Django 5.2.4
- **Frontend**: Bootstrap 5.3.0, Custom CSS
- **Database**: PostgreSQL (production), SQLite (dev)
- **Web Server**: Nginx + Gunicorn
- **OS**: Ubuntu 24.04 LTS
- **Python**: 3.10.11
- **Image Processing**: Pillow (PIL)
- **Rich Text**: Django CKEditor 5
- **Environment**: python-dotenv
- **Typography**: Google Fonts (Ramabhadra)

## 📋 Requirements

- **Python**: 3.10.11
- **Django**: 5.2.4
- **OS**: Ubuntu 24.04 LTS (production)
- **Database**: PostgreSQL 14+
- **Web Server**: Nginx + Gunicorn
- **Additional Python Packages**:
  - Pillow (PIL)
  - python-dotenv
  - django-ckeditor-5
  - psycopg2-binary (PostgreSQL driver)
  - gunicorn (WSGI server)

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/dmouli408/telugu_news_adda.git
cd telugu_news_adda
```

### 2. Create Virtual Environment (Linux/Ubuntu)
```bash
# Create virtual environment with Python 3.10.11
python3.10 -m venv environ

# Activate virtual environment
source environ/bin/activate

# Verify Python version
python --version
# Should show: Python 3.10.11
```

### 3. Install Dependencies (Linux/Ubuntu)
```bash
# Upgrade pip first
pip install --upgrade pip

# Install Python dependencies
pip install -r requirements.txt

# Install system dependencies (if needed)
sudo apt update
sudo apt install python3.10-dev libpq-dev build-essential -y
```

### 4. Environment Configuration (Linux)
```bash
# Copy example environment file
cp .env.example .env

# Edit .env file with nano or vim
nano .env
# or
vim .env

# Set proper file permissions
chmod 600 .env
```

### 5. Database Setup
```bash
# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Load sample data (optional)
python manage.py loaddata sample_data.json
```

### 6. Static Files & Media Setup (Linux)
```bash
# Create media directories
mkdir -p media/posts media/gallery media/ckeditor_uploads

# Set proper permissions
chmod 755 media/
chmod 755 media/posts/
chmod 755 media/gallery/
chmod 755 media/ckeditor_uploads/

# Collect static files
python manage.py collectstatic --noinput
```

### 7. Run Development Server (Linux)
```bash
# Run Django development server
python manage.py runserver 0.0.0.0:8000

# Or for local development only
python manage.py runserver 127.0.0.1:8000

# Check if server is running
curl http://127.0.0.1:8000
```

Visit `http://127.0.0.1:8000` to see your website!

## ⚙️ Configuration

### Environment Variables (.env)

```env
# Django Settings
SECRET_KEY=your-very-secure-secret-key-here
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost,yourdomain.com

# Database Configuration
DATABASE_ENGINE=sqlite3  # or postgresql, mysql
DATABASE_NAME=db.sqlite3
DATABASE_USER=
DATABASE_PASSWORD=
DATABASE_HOST=
DATABASE_PORT=

# Media/Static Files
STATIC_URL=/static/
MEDIA_URL=/media/

# CKEditor Settings
CKEDITOR_MAX_FILE_SIZE=2097152
CKEDITOR_IMAGE_QUALITY=75
CKEDITOR_MAX_IMAGE_SIZE=1024

# Email Configuration
EMAIL_BACKEND=django.core.mail.backends.smtp.EmailBackend
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=your_email@gmail.com
EMAIL_HOST_PASSWORD=your_app_password

# Security Settings (Production)
SECURE_SSL_REDIRECT=False
SESSION_COOKIE_SECURE=False
CSRF_COOKIE_SECURE=False
```

### Database Configurations

#### PostgreSQL (Production - Ubuntu 24.04)
```env
DATABASE_ENGINE=postgresql
DATABASE_NAME=telugu_news_db
DATABASE_USER=postgres
DATABASE_PASSWORD=your_secure_password
DATABASE_HOST=localhost
DATABASE_PORT=5432
```

#### SQLite (Development)
```env
DATABASE_ENGINE=sqlite3
DATABASE_NAME=db.sqlite3
```

## 📁 Project Structure

```
telugu_news_adda/
├── blog/                          # Main blog application
│   ├── management/
│   │   └── commands/
│   │       └── delete_unused_images.py  # Cleanup command
│   ├── migrations/                # Database migrations
│   ├── templates/
│   │   └── blog/
│   │       ├── home.html         # Homepage template
│   │       ├── post_detail.html  # Post detail page
│   │       ├── category_posts.html # Category listing
│   │       ├── create_post.html  # Post creation form
│   │       └── user_post_detail.html # Public post view
│   ├── templatetags/
│   │   └── blog_extras.py        # Custom template tags
│   ├── admin.py                  # Admin configuration
│   ├── forms.py                  # Django forms
│   ├── models.py                 # Database models
│   ├── urls.py                   # URL patterns
│   └── views.py                  # View functions
├── static/                       # Static files
│   ├── default.webp             # Default image
│   ├── ramabhadra-custom.css     # Custom font styles
│   └── ckeditor5/               # CKEditor assets
├── media/                        # User uploaded files
│   ├── posts/                   # Featured images
│   ├── gallery/                 # Gallery images
│   └── ckeditor_uploads/        # CKEditor uploads
├── telugu_news_adda/            # Project configuration
│   ├── settings.py              # Django settings
│   ├── urls.py                  # Main URL configuration
│   └── wsgi.py                  # WSGI configuration
├── .env                         # Environment variables
├── .env.example                 # Environment template
├── .gitignore                   # Git ignore rules
├── manage.py                    # Django management script
└── requirements.txt             # Python dependencies
```

## 🎯 Usage Guide

### Admin Panel
1. Access admin at `/admin/`
2. Login with superuser credentials
3. Manage categories, posts, and users

### Creating Posts
1. Login to admin or use `/create/` endpoint
2. Add title, content, and featured image
3. Optionally add gallery images and YouTube videos
4. Set category and tags
5. Publish or save as draft

### Managing Categories
1. Create hierarchical categories in admin
2. Set category colors and icons
3. Configure homepage display settings
4. Manage category ordering

### Navigation Menu
1. Create menu items in admin
2. Link to categories or external URLs
3. Set menu order and hierarchy

## 🔧 Management Commands

### Git Commands

```bash
# Initialize a new Git repository
git init

# Add all files to staging
git add .

# Commit changes
git commit -m "Initial commit"

# Add remote repository
git remote add origin https://github.com/dmouli408/telugu_news_adda.git

# Push to remote repository
git push -u origin main

# Check repository status
git status

# View commit history
git log --oneline
```

### Clean Up Unused Images

The `delete_unused_images` command helps maintain your media storage by removing orphaned files.

#### Basic Usage
```bash
# 🧪 DRY RUN - See what would be deleted (ALWAYS run this first)
python manage.py delete_unused_images --dry-run

# 📊 Show detailed summary with file counts
python manage.py delete_unused_images --dry-run --show-summary

# 🗑️ Actually delete unused files (run after dry-run)
python manage.py delete_unused_images

# 📈 Delete with summary report
python manage.py delete_unused_images --show-summary
```

#### Target Specific Folders
```bash
# Clean only CKEditor uploads
python manage.py delete_unused_images --folder=ckeditor_uploads --dry-run

# Clean only post featured images
python manage.py delete_unused_images --folder=posts --dry-run

# Clean only gallery images
python manage.py delete_unused_images --folder=gallery --dry-run
```

#### Command Options
| Option | Description | Example |
|--------|-------------|---------|
| `--folder` | Target specific folder | `--folder=posts` |
| `--dry-run` | Preview without deleting | `--dry-run` |
| `--show-summary` | Show detailed statistics | `--show-summary` |

## 🎨 Customization

### Adding New Fonts
1. Add font files to `static/fonts/`
2. Update `ramabhadra-custom.css`
3. Apply font in templates

### Custom Styles
1. Edit `static/custom.css`
2. Use CSS variables for consistent theming
3. Follow Bootstrap 5 conventions

### Template Customization
1. Override templates in `blog/templates/blog/`
2. Use Django template inheritance
3. Customize base.html for global changes

## 📊 Performance Optimization

### Image Optimization
- All images automatically converted to WebP
- Compression quality configurable via environment
- Responsive image serving
- Unused image cleanup

### Database Optimization
- Select_related and prefetch_related usage
- Proper indexing on frequently queried fields
- Pagination for large datasets

### Caching (Production)
```python
# Add to settings.py for production
CACHES = {
    'default': {
        'BACKEND': 'django.core.cache.backends.redis.RedisCache',
        'LOCATION': 'redis://127.0.0.1:6379/1',
    }
}
```

## 🚀 Deployment

### Production Setup on Ubuntu 24.04 VPS

#### 1. System Update & Dependencies
```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install Python 3.10.11 and pip
sudo apt install python3.10 python3.10-venv python3.10-dev python3-pip -y

# Install PostgreSQL
sudo apt install postgresql postgresql-contrib -y

# Install Nginx
sudo apt install nginx -y

# Install system dependencies
sudo apt install build-essential libpq-dev -y
```

#### 2. PostgreSQL Setup
```bash
# Switch to postgres user
sudo -u postgres psql

# Create database and user
CREATE DATABASE telugu_news_db;
CREATE USER telugu_user WITH PASSWORD 'your_secure_password';
GRANT ALL PRIVILEGES ON DATABASE telugu_news_db TO telugu_user;
ALTER USER telugu_user CREATEDB;
\q
```

#### 3. Project Setup
```bash
# Create project directory
sudo mkdir -p /var/www/telugu_news_adda
sudo chown $USER:$USER /var/www/telugu_news_adda

# Clone repository
cd /var/www
git clone https://github.com/dmouli408/telugu_news_adda.git
cd telugu_news_adda

# Create virtual environment
python3.10 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

#### 4. Environment Configuration
```bash
# Create production .env file
cp .env.example .env
nano .env
```

**Production .env:**
```env
SECRET_KEY=your-very-secure-secret-key-here
DEBUG=False
ALLOWED_HOSTS=your-domain.com,www.your-domain.com,your-vps-ip

DATABASE_ENGINE=postgresql
DATABASE_NAME=telugu_news_db
DATABASE_USER=telugu_user
DATABASE_PASSWORD=your_secure_password
DATABASE_HOST=localhost
DATABASE_PORT=5432

STATIC_URL=/static/
MEDIA_URL=/media/

# Security Settings
SECURE_SSL_REDIRECT=True
SESSION_COOKIE_SECURE=True
CSRF_COOKIE_SECURE=True
```

#### 5. Django Setup
```bash
# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Collect static files
python manage.py collectstatic --noinput

# Set permissions
sudo chown -R $USER:www-data /var/www/telugu_news_adda
sudo chmod -R 755 /var/www/telugu_news_adda
```

#### 6. Gunicorn Configuration
```bash
# Create Gunicorn socket file
sudo nano /etc/systemd/system/gunicorn.socket
```

**Gunicorn Socket:**
```ini
[Unit]
Description=gunicorn socket

[Socket]
ListenStream=/run/gunicorn.sock

[Install]
WantedBy=sockets.target
```

```bash
# Create Gunicorn service file
sudo nano /etc/systemd/system/gunicorn.service
```

**Gunicorn Service:**
```ini
[Unit]
Description=gunicorn daemon
Requires=gunicorn.socket
After=network.target

[Service]
User=www-data
Group=www-data
WorkingDirectory=/var/www/telugu_news_adda
ExecStart=/var/www/telugu_news_adda/venv/bin/gunicorn \
          --access-logfile - \
          --workers 3 \
          --bind unix:/run/gunicorn.sock \
          telugu_news_adda.wsgi:application

[Install]
WantedBy=multi-user.target
```

```bash
# Start and enable Gunicorn
sudo systemctl start gunicorn.socket
sudo systemctl enable gunicorn.socket
sudo systemctl daemon-reload
sudo systemctl restart gunicorn
```

#### 7. Nginx Configuration
```bash
# Create Nginx configuration
sudo nano /etc/nginx/sites-available/telugu_news_adda
```

**Nginx Configuration:**
```nginx
server {
    listen 80;
    server_name your-domain.com www.your-domain.com;

    location = /favicon.ico { access_log off; log_not_found off; }
    
    location /static/ {
        root /var/www/telugu_news_adda;
        expires 30d;
        add_header Cache-Control "public, immutable";
    }

    location /media/ {
        root /var/www/telugu_news_adda;
        expires 30d;
        add_header Cache-Control "public, immutable";
    }

    location / {
        include proxy_params;
        proxy_pass http://unix:/run/gunicorn.sock;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }

    # Security headers
    add_header X-Frame-Options "SAMEORIGIN" always;
    add_header X-Content-Type-Options "nosniff" always;
    add_header Referrer-Policy "no-referrer-when-downgrade" always;
    add_header Content-Security-Policy "default-src 'self' http: https: data: blob: 'unsafe-inline'" always;
}
```

```bash
# Enable site
sudo ln -s /etc/nginx/sites-available/telugu_news_adda /etc/nginx/sites-enabled
sudo nginx -t
sudo systemctl restart nginx
```

#### 8. SSL Certificate (Let's Encrypt)
```bash
# Install Certbot
sudo apt install certbot python3-certbot-nginx -y

# Obtain SSL certificate
sudo certbot --nginx -d your-domain.com -d www.your-domain.com

# Test auto-renewal
sudo certbot renew --dry-run
```

#### 9. Firewall Configuration
```bash
# Configure UFW firewall
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw allow 'Nginx Full'
sudo ufw enable
```

### Production Maintenance

#### Service Management
```bash
# Check Gunicorn status
sudo systemctl status gunicorn

# Restart services
sudo systemctl restart gunicorn
sudo systemctl restart nginx

# View logs
sudo journalctl -u gunicorn
sudo tail -f /var/log/nginx/error.log
```

#### Update Deployment
```bash
# Pull latest changes
cd /var/www/telugu_news_adda
git pull origin main

# Activate virtual environment
source venv/bin/activate

# Update dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Collect static files
python manage.py collectstatic --noinput

# Restart services
sudo systemctl restart gunicorn
```

### Production Settings
1. Set `DEBUG=False` in `.env`
2. Configure proper `ALLOWED_HOSTS`
3. Set up SSL certificates
4. Use production database (PostgreSQL/MySQL)
5. Configure email settings
6. Set up static file serving

### Docker Deployment
```dockerfile
FROM python:3.11-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .
RUN python manage.py collectstatic --noinput

EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
```

### Nginx Configuration
```nginx
server {
    listen 80;
    server_name yourdomain.com;
    
    location /static/ {
        alias /path/to/staticfiles/;
    }
    
    location /media/ {
        alias /path/to/media/;
    }
    
    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
```

## � Security Checklist

- [ ] Secret key is secure and not in version control
- [ ] DEBUG=False in production
- [ ] ALLOWED_HOSTS properly configured
- [ ] Database credentials secured
- [ ] SSL/HTTPS enabled
- [ ] CSRF protection enabled
- [ ] XSS protection enabled
- [ ] SQL injection prevention (using ORM)
- [ ] File upload validation
- [ ] Rate limiting implemented

## 🐛 Troubleshooting

### Common Issues

#### Image Upload Problems (Linux)
```bash
# Check media directory permissions
sudo chmod 755 media/
sudo chmod 755 media/posts/
sudo chmod 755 media/gallery/
sudo chown -R $USER:www-data media/

# Check disk space
df -h

# Check if Python can write to media directory
python -c "import os; print(os.access('media', os.W_OK))"
```

#### Database Issues (Linux/PostgreSQL)
```bash
# Check PostgreSQL service
sudo systemctl status postgresql

# Connect to PostgreSQL
sudo -u postgres psql

# Check database connection
python manage.py dbshell

# Reset migrations (development only)
python manage.py migrate --fake blog zero
python manage.py migrate

# Check database permissions
sudo -u postgres psql -c "SELECT datname, datdba, datacl FROM pg_database WHERE datname='telugu_news_db';"
```

#### Static Files Not Loading (Linux/Nginx)
```bash
# Collect static files
python manage.py collectstatic --clear

# Check static files permissions
sudo chmod -R 755 static/
sudo chmod -R 755 staticfiles/

# Check Nginx configuration
sudo nginx -t
sudo systemctl reload nginx

# Check Nginx logs
sudo tail -f /var/log/nginx/error.log
```

#### Git Issues (Linux)
```bash
# If you get permission denied errors
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# If remote already exists
git remote remove origin
git remote add origin https://github.com/dmouli408/telugu_news_adda.git

# If you need to force push (use with caution)
git push --force-with-lease origin main

# Fix file permissions after git operations
find . -type f -name "*.py" -exec chmod 644 {} \;
find . -type d -exec chmod 755 {} \;
```

#### Linux System Issues
```bash
# Check system resources
htop
# or
top

# Check memory usage
free -h

# Check disk usage
df -h
du -sh /var/www/telugu_news_adda/

# Check running processes
ps aux | grep python
ps aux | grep gunicorn
ps aux | grep nginx

# Check network connections
netstat -tlnp | grep :8000
netstat -tlnp | grep :80

# Check system logs
sudo journalctl -u gunicorn.service
sudo journalctl -u nginx.service
```

### Error Messages

#### "ModuleNotFoundError: No module named 'blog'"
- Ensure you're in the correct directory
- Check INSTALLED_APPS in settings.py
- Verify virtual environment is activated: `which python`

#### "ImproperlyConfigured: The SECRET_KEY setting must not be empty"
- Check your .env file exists and contains SECRET_KEY
- Verify python-dotenv is installed
- Check file permissions: `ls -la .env`

#### "Permission denied" errors (Linux)
- Check file ownership: `ls -la`
- Fix permissions: `sudo chown -R $USER:$USER /path/to/project`
- Check directory permissions: `chmod 755 directory_name`

#### "Port already in use" (Linux)
- Find process using port: `sudo netstat -tlnp | grep :8000`
- Kill process: `sudo kill -9 PID`
- Or use different port: `python manage.py runserver 0.0.0.0:8001`

## 🖥️ Linux Quick Reference

### Service Management (Ubuntu 24.04)
```bash
# Check service status
sudo systemctl status gunicorn
sudo systemctl status nginx
sudo systemctl status postgresql

# Start/Stop/Restart services
sudo systemctl start gunicorn
sudo systemctl stop gunicorn
sudo systemctl restart gunicorn

# Enable/Disable auto-start
sudo systemctl enable gunicorn
sudo systemctl disable gunicorn

# View service logs
sudo journalctl -u gunicorn -f
sudo journalctl -u nginx -f
```

### File Operations
```bash
# Find files
find /var/www/telugu_news_adda -name "*.py" -type f
find . -name "*.log" -type f -exec rm {} \;

# Check file permissions
ls -la
stat filename

# Change ownership
sudo chown -R user:group /path/to/directory
sudo chown www-data:www-data /var/www/telugu_news_adda

# Archive and backup
tar -czf backup_$(date +%Y%m%d).tar.gz /var/www/telugu_news_adda
```

### Process Management
```bash
# Monitor processes
ps aux | grep python
ps aux | grep gunicorn
pgrep -f "python manage.py runserver"

# Kill processes
pkill -f "python manage.py runserver"
sudo kill -9 PID

# Monitor system resources
htop
iotop
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Development Guidelines
- Follow PEP 8 style guide
- Add tests for new features
- Update documentation
- Use meaningful commit messages

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Mouli Penumala** - *Initial work* - [dmouli408](https://github.com/dmouli408)

## 🙏 Acknowledgments

- Django community for the excellent framework
- Bootstrap team for the responsive framework
- Google Fonts for Telugu typography
- CKEditor team for the rich text editor
- PIL/Pillow team for image processing

## 📞 Support

For support, email info@telugunewsadda.com or create an issue in the GitHub repository.

## 🔄 Changelog

### v1.0.0 (2025-07-18)
- Initial release
- Basic blog functionality
- Image management system
- Admin interface
- Telugu language support
- Responsive design

---

**Made with ❤️ for Telugu News Community**