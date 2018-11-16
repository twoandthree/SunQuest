# SunQuest
About me app for internship. 
//
//  ViewController.swift
//  Steven Johnston Sunquest Application
//
//  Created by ual-laptop on 11/11/18.
//  Copyright © 2018 Cuxillo. All rights reserved.
//

import UIKit

class ViewController: UIViewController {
    //{} is referred to as closure, or anon, functions.
    let sjohnstonImageView: UIImageView = {
        let imageView = UIImageView(image: #imageLiteral(resourceName: "SJohnston 2018-1"))
        imageView.translatesAutoresizingMaskIntoConstraints = false
        return imageView
    }()
    
    let introductionTextView: UITextView = {
        let textView = UITextView()
        textView.text = "Steven Johnston"
        textView.font = UIFont.boldSystemFont(ofSize: 18)
        textView.translatesAutoresizingMaskIntoConstraints = false
        textView.textAlignment = .center
        textView.isEditable = false
        textView.isScrollEnabled = false
        return textView
    }()

    override func viewDidLoad() {
        super.viewDidLoad()
        view.backgroundColor = .green
        
        view.addSubview(sjohnstonImageView)
        view.addSubview(introductionTextView)
        
        setupLayout()
        
    }
    
    private func setupLayout() {
        
        sjohnstonImageView.centerXAnchor.constraint(equalTo:
            view.centerXAnchor).isActive = true
        sjohnstonImageView.topAnchor.constraint(equalTo: view.topAnchor, constant:
            100).isActive = true
        sjohnstonImageView.widthAnchor.constraint(equalToConstant:
            227.5).isActive = true
        sjohnstonImageView.heightAnchor.constraint(equalToConstant:
            253.75).isActive = true
        
        introductionTextView.topAnchor.constraint(equalTo:
            sjohnstonImageView.bottomAnchor, constant: 80).isActive = true
        introductionTextView.leftAnchor.constraint(equalTo:
        view.leftAnchor).isActive = true
        introductionTextView.rightAnchor.constraint(equalTo:
        view.rightAnchor).isActive = true
        introductionTextView.bottomAnchor.constraint(equalTo:view.bottomAnchor, constant: 0).isActive = true
    }

//    override func didReceiveMemoryWarning() {
//        super.didReceiveMemoryWarning()
//        // Dispose of any resources that can be recreated.
//    }


}
