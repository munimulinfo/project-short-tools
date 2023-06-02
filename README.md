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
    
    ****How to use React Hook form ************
    search react hook form and instal 
    import useForm 
       import { useForm } from 'react-hook-form'; component head;
       const { register, handleSubmit, watch, resetField, formState: { errors } } = useForm(); componet on;
       onSubmit={handleSubmit(onSubmit)} form cotation in and call();
       <div className="form-control">
       <label className="label"> <span className="label-text">Email</span></label>
       <input type="email" name='email' {...register("email", { required: true })} placeholder="Type here" className='h-[50px] border-r-2 rounded-lg bg-white border          pl-5' />
      {errors.email && <span className='text-red-600 animate-pulse'>Email is required</span>}
      </div>
     onclick handle reset button and field reset them
        resetField, this props use UseForm
       const handleClick = () => resetField("name","email", "password");
      onClick={handleClick}
******************Private route*********************
import { useContext } from "react";
import { AuthContext } from "../providers/AuthProvider";
import { Navigate, useLocation } from "react-router";


const PrivateRoute = ({ children }) => {
    const { user, loading } = useContext(AuthContext);
    const location = useLocation();

    if(loading){
        return <progress className="progress w-56"></progress>
    }

    if (user) {
        return children;
    }
    return <Navigate to="/login" state={{from: location}} replace></Navigate>
};

export default PrivateRoute;
********************active LInk***********************
import React from 'react';
import { NavLink } from 'react-router-dom';
const ActiveLink = ({to, children}) => {
    return (
    <NavLink
    to={to}
    className={({ isActive}) => isActive ? "text-white" : ''}>
    {children}
    </NavLink>
    );
};

export default ActiveLink;
