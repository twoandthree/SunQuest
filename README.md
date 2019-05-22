//
//  ViewController.swift
//  SJohnston-SunQuest-Portfolio
//
//  Created by ual-laptop on 5/19/19.
//  Copyright © 2019 IUNI. All rights reserved.
//

import UIKit

class ViewController: UIViewController {
    
    // let's avoid polluting viewDidLoad
    // {} is referred to as closure, or anon functions
    let SJPortfolioImageView: UIImageView = {
        let imageSJ: UIImage = #imageLiteral(resourceName: "sjohnston")
        let SJimageView = UIImageView(image: imageSJ)
        //this enables autolayout for our SJimageView
        SJimageView.translatesAutoresizingMaskIntoConstraints = false
        SJimageView.contentMode = .scaleAspectFit
        return SJimageView
    }()
    
    let objectiveTextView: UITextView = {
       let objectivetextView = UITextView()
        objectivetextView.text = "Objective: attain internship at SunQuest."
        objectivetextView.font = UIFont.boldSystemFont(ofSize: 18)
        objectivetextView.font = UIFont.italicSystemFont(ofSize: 18)
        objectivetextView.translatesAutoresizingMaskIntoConstraints = false
        objectivetextView.textAlignment = .center
        return objectivetextView
    }()
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.

        view.addSubview(SJPortfolioImageView)
        view.addSubview(objectiveTextView)
        
        setupLayout()
    }
    
    private func setupLayout() {
        let topImageContainerView = UIView()
        topImageContainerView.backgroundColor = .blue
        view.addSubview(topImageContainerView)
//        topImageContainerView.frame = CGRect(x: 0, y: 0, width: 100, height: 100)
        // Enable Auto Layout
        topImageContainerView.translatesAutoresizingMaskIntoConstraints = false
        
        topImageContainerView.topAnchor.constraint(equalTo:view.topAnchor).isActive = true
        
        topImageContainerView.leadingAnchor.constraint(equalTo:view.leadingAnchor).isActive = true
        topImageContainerView.trailingAnchor.constraint(equalTo:view.trailingAnchor).isActive = true
//        topImageContainerView.leftAnchor.constraint(equalTo: view.leftAnchor).isActive = true
//        topImageContainerView.rightAnchor.constraint(equalTo: view.rightAnchor).isActive = true
        
        
        
        topImageContainerView.heightAnchor.constraint(equalTo: view.heightAnchor, multiplier: 0.5).isActive = true
        
//        SJPortfolioImageView.centerXAnchor.constraint(equalTo: view.centerXAnchor).isActive = true
//        SJPortfolioImageView.topAnchor.constraint(equalTo: view.topAnchor, constant: 100).isActive = true
//        SJPortfolioImageView.widthAnchor.constraint(equalToConstant: 253.5).isActive = true
//        SJPortfolioImageView.heightAnchor.constraint(equalToConstant: 253.75).isActive = true
        
        objectiveTextView.topAnchor.constraint(equalTo: SJPortfolioImageView.bottomAnchor, constant:70).isActive = true
        objectiveTextView.leftAnchor.constraint(equalTo:view.leftAnchor).isActive = true
        objectiveTextView.rightAnchor.constraint(equalTo:view.rightAnchor).isActive = true
        objectiveTextView.bottomAnchor.constraint(equalTo:view.bottomAnchor, constant:0).isActive = true
    }

}
