# Front-End-boxzi

class DoctorProfile:  
    def __init__(self, name, specialty, likes=0):  
        self.name = name  
        self.specialty = specialty  
        self.likes = likes  

    def __str__(self):  
        return f"{self.name} - {self.specialty} - Likes: {self.likes}"  

# مثالی از فهرست پروفایل‌ها  
profiles = [  
    DoctorProfile("Dr. John", "Cardiologist", 20),  
    DoctorProfile("Dr. Sarah", "Dermatologist", 15),  
    DoctorProfile("Dr. Mike", "Pediatrician", 10),  
    DoctorProfile("Dr. Lisa", "Psychiatrist", 25),  
]  

def sort_profiles_by_likes(profiles, desc=False):  
    return sorted(profiles, key=lambda x: x.likes, reverse=desc)  

# نمایش پروفایل‌ها  
for profile in profiles:  
    print(profile)  

print("\n")  

# مرتب‌سازی و نمایش پروفایل‌ها بر اساس تعداد لایک  
sorted_profiles_desc = sort_profiles_by_likes(profiles, desc=True)  
for profile in sorted_profiles_desc:  
    print(profile)
