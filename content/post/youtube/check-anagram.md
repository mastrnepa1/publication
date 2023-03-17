---
title: "Check if 2 Strings are Anagram or not" # Title of the blog post.
date: 2023-03-17T07:43:09+05:45 # Date of post creation.
description: "How to check whether two strings are anagram or not in Java." # Description used for search engine.
author: "Satya Raj Awasthi"
featured: true # Sets if post is a featured post, making appear on the home page side bar.
draft: false # Sets whether to render this page. Draft of true will not be rendered.

thumbnail: "/images/checking whether two strings are anagram or not mastr.png" # Sets thumbnail image appearing inside card on homepage.
keywords: ["checking if two strings are anagram or not","checking anagram using sorting","check if strings are anagram in java","check anagram mastr","mastr","dsa java"]
categories:
  - interview questions
tags:
  - java
  - check anagram
# comment: false # Disable comment if false.
---

![Check whether two strins are anagram or not.](http://mastr.satyarajawasthi.com.np/images/checking%20whether%20two%20strings%20are%20anagram%20or%20not%20mastr.png)
Are you preparing for interview exams for internships, traineeship or other entry level position. The you may face this question in your technical round. 

Lets see how we can check whether two strings are anagram or not. Before diving into, lets break the title.

**What does Anagram String Mean ?**

Lets see with an example. Let, first string be *mastr* and second string be *amtsr*. Then this two strings are anagram.

So, we got that Anagram strings are **"Strings that are made up of same characters but characters in different sequence."**

{{% notice tip "We will use sorting method to do it. So then for it we will" %}}
  + sort strings
  + compare sorted strings
{{% /notice %}}


The source code is here.
```java
import java.util.Arrays;
import java.util.Scanner;

public class CheckAnagram {

    public static void main(String[] args) {
        /*
        Checking whether two strings are anagram or not.
        hello
        lolhe

        Sorting:
        -> sort strings
        -> compare sorted strings
         */
        // Take 2 string inputs
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter 2 strings:");
        String str1 = scanner.next();
        String str2 = scanner.next();
        scanner.close();

        // convert strings to character arrays for sorting
        char [] arr1 = str1.toCharArray();
        char [] arr2 = str2.toCharArray();

        // sorting character arrays in alphabetical order.
        Arrays.sort(arr1);
        Arrays.sort(arr2);

        // check and display whether strings are anagram or not.
        if (checkAnagram(arr1, arr2)) {
            System.out.println("Strings are anagram.");
        }
        else {
            System.out.println("Strings are not anagram.");
        }
    }

    //checkAnagram method to check
    static boolean checkAnagram(char[] str1, char[] str2){
        // if length of strings / character arrays are not equal strings will never be anagram
        if (str1.length != str2.length){
            return false;
        }
        // check each index of both arrays, will never be anagram if each index of both strings have different character
        for (int i = 0; i < str1.length; i++) {
            if (str1[i] != str2[i]){
                return false;
            }
        }
        return true;
    }
}
```

THank you for reading. *Watch video to be more clear.*
{{< youtube kuF3mobdNuI >}}