# Problem 4 : Palindrome


def my_palindrome(number):
  num_str = str(number)

  reverse_str = num_str[::-1]

  if num_str == reverse_str:
    return True
  else:
    return False


print(my_palindrome(121))
print(my_palindrome(123))

# Problem 5 : Average Age

company = {
  'employees': {
    'John': {
      'age': 35,
      'job_title': 'Manager'
    },
    'Emma': {
      'age': 28,
      'job_title': 'Software Engineer'
    },
    'Kelly': {
      'age': 41,
      'job_title': 'Senior Developer'
    },
    'Sam': {
      'age': 30,
      'job_title': 'Software Engineer'
    },
    'Mark': {
      'age': 37,
      'job_title': 'Senior Manager'
    },
    'Sara': {
      'age': 32,
      'job_title': 'Software Engineer'
    },
  }
}

import math


def my_avg(company):
  total_age = 0
  count = 0

  for employee, details in company['employees'].items():
    job_title = details['job_title']
    if job_title.startswith('S'):
      total_age += details['age']
      count += 1

  if count == 0:
    return 0

  avg_age = total_age / count
  avg_age = math.ceil(avg_age)
  return avg_age


print(my_avg(company))
