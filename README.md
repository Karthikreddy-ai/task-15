user_profiles = {}
def add_user(user_id, name):
    user_profiles[user_id] = name
    print(f"Added user: {user_id} → {name}")
    print("Current profiles:", user_profiles)

def get_user(user_id):
    if user_id in user_profiles:
        print(f"User ID {user_id} belongs to: {user_profiles[user_id]}")
    else:
        print(f"User ID {user_id} not found.")
def update_user(user_id, new_name):
    if user_id in user_profiles:
        user_profiles[user_id] = new_name
        print(f"Updated user {user_id} → {new_name}")
    else:
        print(f"User ID {user_id} not found.")
    print("Current profiles:", user_profiles)
def remove_user(user_id):
    if user_id in user_profiles:
        removed_name = user_profiles.pop(user_id)
        print(f"Removed user: {user_id} → {removed_name}")
    else:
        print(f"User ID {user_id} not found.")
    print("Current profiles:", user_profiles)
add_user(101, "Alice")
add_user(102, "Bob")
add_user(103, "Charlie")

get_user(102)
get_user(200)  # Non-existent ID
update_user(103, "Charlotte")
update_user(200, "David")  # Non-existent ID
remove_user(101)
remove_user(300)  # Non-existent ID
