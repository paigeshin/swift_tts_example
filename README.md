# swift_tts_example

https://github.com/proscus0706/swift_tts_example/tree/master


    //
    //  ViewController.swift
    //  ios_tts_example
    //
    //  Created by shin seunghyun on 2020/04/11.
    //  Copyright © 2020 shin seunghyun. All rights reserved.
    //

    import UIKit
    import AVFoundation

    class ViewController: UIViewController {

        override func viewDidLoad() {
            super.viewDidLoad()
            let utterance = AVSpeechUtterance(string: "안녕하세요 한국인이에요")
            
            /*
             en-US
             fr-FR
             ko-KR
             jp-JA
             de-DE
             es-ES
             */
            
            utterance.voice = AVSpeechSynthesisVoice(language: "ko-KR")
            utterance.rate = 0.5

            let synthesizer = AVSpeechSynthesizer()
            synthesizer.speak(utterance)
        }


    }
