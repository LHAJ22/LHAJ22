import random

def welcome_message():
    print("مرحباً! أنا هنا لتوليد أرقام عشوائية لك ضمن نطاق محدد.")

def get_random_number(start, end):
    return random.randint(start, end)

def main():
    welcome_message()
    while True:
        try:
            start = int(input("أدخل البداية للنطاق: "))
            end = int(input("أدخل النهاية للنطاق: "))
            if start > end:
                print("البداية يجب أن تكون أقل أو تساوي النهاية. حاول مرة أخرى.")
                continue
            random_number = get_random_number(start, end)
            print(f"الرقم العشوائي بين {start} و {end} هو: {random_number}")
        except ValueError:
            print("يرجى إدخال أرقام صحيحة.")
        
        again = input("هل ترغب في توليد رقم آخر؟ (نعم/لا): ").strip().lower()
        if again != 'نعم':
            print("إلى اللقاء!")
            break

if __name__ == "__main__":
    main()