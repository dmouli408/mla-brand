
# MLA Personal Branding App

Designed by Dasari Mouli

# 🇮🇳 MLA Personal Branding App – Development Guide

A mobile and web platform to showcase an MLA’s initiatives, engage citizens, and push real-time updates using **Django**, **Flutter**, **Firebase**, and **GitHub Pages**.

---

## 🧱 1. Project Setup

- ✅ Create GitHub repositories:
  - `mla-backend` (Django)
  - `mla-app` (Flutter)
  - `mla-brand.github.io` (for GitHub Pages)

- ✅ Choose your hosting:
  - Free: PythonAnywhere or Render
  - VPS: Hostinger / DigitalOcean

- ✅ Configure domain (optional)
- ✅ Initialize Flutter and Django apps
- ✅ Set up Firebase for push notifications

---

## 👥 2. User Management (Django Admin Panel)

Allow only **Media Team** to log in and manage content:

```python
class User(AbstractUser):
    ROLE_CHOICES = (
        ('admin', 'Admin'),
        ('media', 'Media Team'),
    )
    role = models.CharField(max_length=10, choices=ROLE_CHOICES, default='media')
```

- Enable login via Django Admin
- Restrict each media user to manage only their posts
- Create superuser (`python manage.py createsuperuser`) for full control

---

## 📰 3. Content Posting (Django)

```python
class Post(models.Model):
    title = models.CharField(max_length=255)
    description = models.TextField()
    image = models.ImageField(upload_to='posts/')
    created_by = models.ForeignKey(User, on_delete=models.CASCADE)
    created_at = models.DateTimeField(auto_now_add=True)
```

- Use `admin.py` customization to restrict `media` users to only their own posts
- Upload posts with images and descriptions

---

## 🗃️ 4. Static Export (Optional for GitHub Pages)

- Export posts and images to:
  - `posts.json`
  - `/images/post1.jpg`, `/images/post2.jpg`
- Push static content to GitHub Pages repo

---

## 🌍 5. Hosting Static Content (GitHub Pages)

- Create repo: `mla-brand.github.io`
- Enable GitHub Pages in repo settings
- Serve static content at `https://mla-brand.github.io`

---

## 📱 6. Flutter App Setup

- Use `http` package to fetch JSON
- Display:
  - 🏠 Homepage
  - 📸 Gallery
  - 📜 Post detail
  - 📅 Events

```dart
final response = await http.get(Uri.parse('https://mla-brand.github.io/posts.json'));
```

---

## 🔔 7. Push Notifications (Firebase FCM)

```python
def send_fcm_notification(title, body):
    headers = {
        'Authorization': 'key=YOUR_SERVER_KEY',
        'Content-Type': 'application/json',
    }
    data = {
        'to': '/topics/all',
        'notification': {'title': title, 'body': body},
    }
    requests.post('https://fcm.googleapis.com/fcm/send', headers=headers, json=data)
```

---

## 🧪 8. Load Testing (Optional)

- Use **Locust** or **JMeter**
- Simulate 1000–5000 users
- Monitor VPS resource usage

---

## ⚡ 9. Optimization Tips

- Pagination
- Caching (Redis)
- Image compression
- Index `created_at`, `created_by`

---

## 🚀 10. Deployment & Maintenance

- Deploy Django (Gunicorn + Nginx or PythonAnywhere)
- Sync content to GitHub Pages
- Automate with GitHub Actions or scripts

---

## 👨‍💻 Developer

**Dasari Mouli**  
*Full Stack Developer*  
Project Head – Digital Assistant Community  
📍 Vijayawada, Andhra Pradesh, India

> “Building digital bridges for smarter local governance.”
