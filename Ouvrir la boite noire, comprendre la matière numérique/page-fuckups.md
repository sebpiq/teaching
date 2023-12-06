
```
const shake2 = (selector, stepMs, shakeAmpPx, scaleAmp, hasTransitions) => {
    const _rand = (amp) => amp * (Math.random() * 2 - 1)
    const elems = document.querySelectorAll(selector)
    if (hasTransitions) {
        elems.forEach(d => d.style.transition = `transform ${stepMs / 1000}s`)//<property> <duration> <timing-function> <delay>
    }
    setInterval(() => document.querySelectorAll(selector).forEach(d => {
        const [x, y] = (d.style.transform || 'translate(0px, 0px) scale(1)')
            .split(' scale')[0]
            .slice('translate('.length, -')'.length)
            .split(', ').map(v => parseInt(v))
        d.style.transform = `translate(${x + shakeAmpPx + _rand(shakeAmpPx)}px, ${y + shakeAmpPx + _rand(shakeAmpPx)}px) scale(${1 + _rand(scaleAmp)})`
    }), stepMs)
}
// shake('div', 100, 1, 0.05, false)



const colors = (selector, stepMs, hasTransitions) => {
    const _colorPart = () => Math.floor(parseInt('ff', 16) * Math.random()).toString(16).padEnd('0')
    let elems = document.querySelectorAll(selector)
    if (hasTransitions) {
        elems.forEach(d => d.style.transition = `color ${stepMs / 1000}s, background-color ${stepMs / 1000}s`)//<property> <duration> <timing-function> <delay>
    }
    setInterval(() => document.querySelectorAll(selector).forEach(d => {
        d.style.color = '#' + _colorPart() + '00' + _colorPart() + _colorPart()
        d.style.backgroundColor = '#' + _colorPart() + '00' + _colorPart() + _colorPart()
    }), stepMs)
}
// colors('a', 130, false)
// colors('h1', 120, false)
// colors('span', 110, false)
// colors('div', 100, false)


// infiniteZoom(15000, 0.02, 40, 120, 3) 
const infiniteZoom = (stepMs, scale0, scale1, rotation, frequency) => {
    const transitionFunc = 'cubic-bezier(1.000, 0.025, 0.950, 0.115)'
    const html = document.body.innerHTML
    document.body.querySelectorAll('script').forEach(e => e.remove())
    document.body.innerHTML = ''
    document.body.style.height = '100vh'
    document.body.style.overflow = 'hidden'
    document.body.style.transformOrigin = 'center center'

    const _transform = (root, initialize) => {
        root.style.transition = `transform ${stepMs / 1000}s ${transitionFunc}`
        root.style.transformOrigin = 'center center'
        root.style.height = '100vh'
        root.style.width = '100vw'
        root.style.overflow = 'hidden'
        root.style.position = 'fixed'
        root.style.top = '0'
        root.style.left = '0'
        if (initialize) {
            root.style.transform = `scale(${scale0}) rotate(0deg)`
        }
        setTimeout(() => {
            root.style.transform = `scale(${scale1}) rotate(${rotation}deg)`
        }, 1)
    }

    const _iter = (initialize = true) => {
        const newPage = document.createElement('div')
        newPage.innerHTML = html
        document.body.appendChild(newPage)
        _transform(newPage, initialize)
        setTimeout(() => {
            newPage.remove()
        }, stepMs + 1000)
    }

    setInterval(_iter, stepMs / frequency)

    _iter(document.body, false)
}


const whirl = () => {
    document.querySelectorAll('*').forEach(el => {
        const spinning = [
            { transform: "rotate(0) scale(1)" },
            { transform: "rotate(360deg) scale(0)" },
        ]
          
        const timing = {
            duration: 10000,
            iterations: 1,
        }
        el.style.transformOrigin = '50vw 50vh'
        el.animate(spinning, timing)
    })    
}

const richWhiteMales = () => {
    document.querySelectorAll('img').forEach(img => {
        const urls = [
            // Zuck
            'https://static.businessinsider.com/image/55835f976bb3f786770aa3ad/image.jpg',
            'https://api.time.com/wp-content/uploads/2016/01/ap_794116323555.jpg',
            'https://static3.businessinsider.com/image/5aabc355cc502925008b46aa-1725/rtr49i7z.jpg',
            'https://technology.inquirer.net/files/2017/02/Facebook-Zuckerberg.jpg',
            'http://static1.businessinsider.com/image/552da630ecad04423c180c63-1977/mark-zuckerberg-393.jpg',
            'https://i.insider.com/53d2b0dbeab8ea563559b0b0',
            'https://cdn.cnn.com/cnnnext/dam/assets/170622131016-02-zuckerberg-interview-color-super-tease.jpg',
            'https://clipground.com/images/mark-zuckerberg-png-6.png',
            'https://api.time.com/wp-content/uploads/2016/01/ap_794116323555.jpg',
    
            // Bezos
            'https://nypost.com/wp-content/uploads/sites/2/2020/06/Bezos-Smile-2.jpg?quality=90&strip=all',
            'https://observer.com/wp-content/uploads/sites/2/2019/06/gettyimages-1032941844.jpg?quality=80&strip',
            'https://i.insider.com/5caeed65c57fa612d34e8cc3?width=1200',
            'https://s3.scoopwhoop.com/anj/photo/cc041081-6374-4e95-90ae-86711d48c680.jpg',
            'https://observer.com/wp-content/uploads/sites/2/2019/10/gettyimages-1079571578-e1572031138891.jpg?resize=320',
            'https://image.cnbcfm.com/api/v1/image/105462405-1537464466367gettyimages-1036099120.jpeg?v=1538582969&w=1400&h=950',
            'https://observer.com/wp-content/uploads/sites/2/2018/11/gettyimages-1032942782.jpg?resize=2048',
            'https://static3.businessinsider.com/image/5bb4ff979a4ab834ec62fd88-2400/jeff-bezos.jpg',
    
            // Musk
            'https://i.insider.com/5fa27f2d1df1d50018218c35?format=jpeg',
            'https://cdn.cnn.com/cnnnext/dam/assets/180907100732-elon-musk-smokes-marijuana-podcast-1-large-169.jpg',
            'https://nypost.com/wp-content/uploads/sites/2/2021/04/elon-musk-010.jpg?quality=90&strip=all',
            'https://www.yourtechstory.com/wp-content/uploads/2020/04/spacex-ceo-elon-musk-2020.jpg',
            'https://www.pulseheadlines.com/wp-content/uploads/2017/01/Elon-Musk.jpg',
            'https://www.manners.nl/wp-content/uploads/2020/12/Elon-Musk-SpaceX.jpg',
            'https://www.financemagnates.com/wp-content/uploads/2020/12/Elon-Musk.jpg',
            'https://static5.businessinsider.com/image/5c754dd71631a378ce205226-1190-625/elon-musks-erratic-twitter-behavior-escalated-wednesday-when-he-changed-his-name-to-elon-tusk.jpg',
            'http://static1.businessinsider.com/image/57ed0ffeb0ef973f1b8b8b8a-1219/rtr49m2y.jpg'
    
        ]
        img.src = urls[Math.floor(Math.random() * urls.length)]
    })
}

const eggplants = () => {
    document.body.querySelectorAll('*').forEach(el => {
        if (['style', 'script'].includes(el.tagName)) {
            return
        }
        if (el.textContent.length && el.children.length === 0) {
            el.textContent = Array.from(el.textContent).map(() => '🍆').join('')
        }
    })
}
```