# project-short-tools
passwrod visula show and hide button code 
 
   const [password, setPassword] = useState(''); const [showPassword, setShowPassword] = useState(false);

const togglePasswordVisibility = () => { setShowPassword(!showPassword); };

<input type={showPassword ? 'text' : 'password'} value={password} onChange={(e) => setPassword(e.target.value)} placeholder="Enter your password" className="input input-bordered"/> {showPassword ? 'Hide Password' : 'Show Password'}

 <input type={showPassword ? 'text' : 'password'} value={password} onChange={(e) => setPassword(e.target.value)} placeholder="Enter your password" 
 className="input input-bordered"/>
 <button onClick={togglePasswordVisibility}>{showPassword ? 'Hide Password' : 'Show Password'}</button>
 
 Navbar hide code to children page useLOcation Hokks
 
     const location = useLocation();
     const noHeaderfooter = location.pathname.includes('login');
    return (
         <div>
           { noHeaderfooter || <Navbar></Navbar>}
            <Outlet></Outlet>
            {noHeaderfooter || <Footer></Footer>}
         </div>
    );
    
    button disabled kivabe korbo tar shor tecknik 
    const [disabled, setDisabled] = useState(true);
    input disabled={disabled}
    okk button is disaable
